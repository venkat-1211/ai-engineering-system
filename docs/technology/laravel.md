# Laravel Engineering Standard

Apply only when Laravel is present. Verify Laravel and PHP versions before using version-specific APIs.

- Follow the installed version's conventions and the existing application structure.
- Use routes, middleware, controllers, Form Requests, policies/gates, services/actions, jobs, events, resources and Eloquent where they add clear value.
- Keep controllers focused on HTTP orchestration. Avoid needless repository abstractions that merely wrap Eloquent.
- Validate request data and authorize every protected operation server-side.
- Enforce ownership and tenant scoping in queries; never rely on frontend filtering.
- Use validated data and explicit mass-assignment protection. Never trust client-supplied role, tenant, price, permission or ownership fields.
- Use migrations for schema changes; plan indexes, transactions, rollback/forward recovery and deployment compatibility.
- Avoid N+1 queries with deliberate eager loading; paginate unbounded data.
- Treat queued jobs as at-least-once unless proven otherwise. Make retryable jobs idempotent; define timeout, backoff and failure handling.
- Prevent overlapping scheduled work where necessary.
- Use supported authentication, secure session/cookie settings, CSRF protection and rate limits for login, OTP and sensitive endpoints.
- Validate uploads and enforce private-file authorization.
- Keep environment values in config; do not call `env()` throughout application code.
- Use explicit HTTP timeouts and safe handling for integrations. Do not expose stack traces or debug output in production.
- Inspect Composer, PHPUnit/Pest, CI and installed Laravel version before choosing test commands. Test policies, tenant isolation, validation, transactions, jobs and API behavior.
- Never run destructive or production migrations without explicit approval.

## SPA authentication, CORS and separate frontend/backend deployments
Apply only when a browser frontend (for example a SPA) calls a Laravel backend. Do not assume Laravel Sanctum is required or installed. First inspect the installed Laravel version, `composer.json`/lockfile, the existing authentication architecture (sessions, Sanctum, Passport, custom tokens), `config/` files, and how the frontend and backend are hosted and served. Verify configuration keys and behavior against the installed version's documentation.

- **First-party SPA, cookie-based:** where the frontend and backend share a registrable domain, prefer cookie/session authentication (for example Sanctum's SPA mode, if installed or approved) over storing bearer tokens in browser storage.
- **Stateful domains:** configure the list of trusted frontend hosts explicitly for the environment; do not use broad or wildcard host patterns.
- **CORS:** allow only explicit, environment-specific origins, methods and headers. **Never use a wildcard origin (`*`) together with credentialed requests** (cookies or authorization headers sent by the browser), and do not reflect arbitrary request origins.
- **Credentialed requests:** enable credential support only when cookie authentication requires it, and make the frontend send credentials explicitly.
- **CSRF:** for cookie-authenticated state-changing requests, obtain the CSRF cookie before login and send the token header the installed version expects; keep CSRF middleware active. Do not disable CSRF protection to make a frontend work.
- **Cookie and session configuration:** use `Secure` cookies over HTTPS, `HttpOnly` for the session cookie, a deliberate `SameSite` value, and a session domain that matches the real deployment. Cross-site setups needing `SameSite=None` require HTTPS and a documented justification. Keep these values in environment configuration, not hard-coded.
- **Separate deployments:** document frontend and backend origins, subdomain relationships, proxy and TLS termination (trusted proxies), and the cookie domain per environment (local, staging, production). Test cross-origin behavior in an environment that resembles production.
- **Token-based authentication:** use API tokens only where justified (third-party or mobile clients, non-browser consumers, different registrable domains without a cookie option). Scope and expire tokens, store them securely, never expose them in URLs or logs, and support revocation. Do not store long-lived tokens in browser local storage without an approved threat assessment.
- **Authorization:** SPA authentication does not replace server-side policy, gate and tenant checks on every API route.
- **Rate limiting and errors:** apply rate limits to login and token endpoints; do not leak whether accounts exist.
- **Tests:** cover authenticated and unauthenticated access, CSRF failure, disallowed origins, credentialed-request behavior, logout and token revocation, using test configuration only.
