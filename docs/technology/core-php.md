# Core PHP Engineering Standard

Apply when PHP code is present. Laravel projects also use `laravel.md`.

- Verify PHP version from manifests, runtime configuration, CI or deployment files. Use only syntax/APIs supported by that version.
- Follow Composer, PSR-4 autoloading, namespaces and existing style. Avoid deprecated APIs.
- Separate presentation, business rules, persistence and infrastructure according to the existing architecture.
- Prefer cohesive classes/functions and explicit dependency boundaries; avoid globals, service locators and unnecessary interfaces.
- Treat request data, headers, cookies, uploads, CLI arguments and external data as untrusted.
- Validate at boundaries; encode output for its actual context.
- Use PDO prepared statements or trusted parameter binding. Never concatenate untrusted data into SQL, shell commands, paths or dynamic code.
- Use `password_hash()` / `password_verify()` and `random_bytes()` for security-sensitive randomness.
- Enforce server-side authorization and CSRF defenses for cookie-authenticated state-changing requests.
- Do not suppress errors with `@` or silently ignore exceptions. Return safe errors and log redacted diagnostics.
- Use transactions for related writes that must be atomic.
- Validate uploads, generate server-side names, prevent executable uploads and path traversal, and authorize file access.
- Keep secrets outside source control. Review package maintenance, license and vulnerabilities before adding dependencies.
- Add tests for business rules, validation, authorization and failure paths.

## Sessions, cookies and authentication state
Verify the PHP version and the actual environment configuration (`php.ini`, runtime settings, framework or CMS session handling) before changing any session setting. Do not assume a setting is available or already configured. These rules apply to hand-written PHP session handling; if a framework or CMS manages sessions, follow its mechanism and its standard instead.

- Protect against session fixation: accept only server-generated session IDs and enable strict session ID mode where the PHP version and environment support it.
- Regenerate the session ID after login, after privilege or role changes and after other authentication state changes; delete the old session data as appropriate.
- Use secure cookie attributes: `HttpOnly`; `Secure` when served over HTTPS (production should use HTTPS); `SameSite` set deliberately (`Lax` or `Strict`, or `None` only with `Secure` and a justified cross-site need). Set an explicit cookie path and domain scope appropriate to the application.
- Restrict sessions to cookies (do not pass session IDs in URLs). Never expose session identifiers in URLs, logs, error messages, responses or client-side scripts.
- Define idle and absolute session lifetimes appropriate to the sensitivity of the application, and enforce expiration server-side.
- Store only the minimum authentication state in the session (such as a user identifier and authentication time), and re-check authorization on the server for each protected request rather than trusting stale session data.
- Protect all state-changing requests with CSRF tokens that are unpredictable, bound to the session and verified server-side; do not use GET for state changes. `SameSite` is defence in depth, not a replacement.
- Implement logout safely: clear the session data, invalidate the session server-side, expire the session cookie, and require a state-changing (non-GET) request where practical.
- Secure the session storage location and permissions; avoid sharing it across applications; rate limit login attempts.
- Test fixation, ID regeneration, expiry, logout and CSRF failure paths.
