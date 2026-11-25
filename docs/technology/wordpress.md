# WordPress Engineering Standard

Apply only when WordPress is present (for example `wp-config.php`, `wp-content/`, a theme with `style.css` headers or a plugin with a plugin header). Do not apply Laravel or other framework architecture to WordPress. Use together with `core-php.md`, `mysql.md`, `javascript-typescript.md` and `html-css-bootstrap-responsive-ui.md` where those technologies are present.

## Discovery
- Verify WordPress core, PHP and database versions from the installed code, `readme`/plugin/theme headers, Composer files, CI or the environment. Do not assume newer core APIs exist.
- Identify whether the work is a theme, child theme, block theme, plugin, mu-plugin or core-adjacent configuration. Inspect the existing implementation, active plugins and theme before changing anything.
- Never edit WordPress core files. Put changes in a theme, child theme or plugin.

## Architecture and conventions
- Follow the WordPress PHP, JavaScript, CSS and HTML coding standards and the project's existing style and naming.
- Prefix functions, classes, hooks, options, post meta, transients and handles to avoid collisions; use namespaces or classes where the project does.
- Keep plugin logic in plugins and presentation in themes. Do not put business logic that must survive a theme switch in a theme.
- Prefer built-in WordPress APIs (Options, Settings, Transients, HTTP, Filesystem, REST, Query, Shortcode, Block and Cron APIs, `WP_Query`, `wp_enqueue_*`) over custom implementations. Confirm an API exists in the installed version before using it.
- Do not use direct includes of core files or hard-coded paths/URLs; use the path and URL helper functions.

## Themes and plugins
- Enqueue scripts and styles through the enqueue functions with explicit dependencies and versions; do not hard-code tags in templates.
- Use child themes for customizing third-party themes. Use template hierarchy and template parts as the theme already does.
- Provide activation, deactivation and uninstall behavior deliberately; uninstall must not silently delete user data without approval.
- Support internationalization using text domains where the project does.

## Hooks (actions and filters)
- Use actions for side effects and filters for transforming values; filters must return a value.
- Register hooks with explicit priorities and correct argument counts. Do not remove or override other plugins' hooks without understanding the effect.
- Do not run expensive work on hooks that fire on every request. Document custom hooks you add.

## Nonces and CSRF
- Protect state-changing requests (forms, admin actions, AJAX) with nonces and verify them server-side before acting.
- A nonce is not authorization; always combine it with a capability check.
- Do not use GET requests for state changes.

## Capabilities and authorization
- Check capabilities with the capability APIs for every admin page, form handler, AJAX handler and REST route. Use the least capability that fits the action.
- For object-level actions, check capability against the specific object. Do not rely on hiding menus or UI.
- Never trust client-supplied user IDs, roles or capabilities.

## Sanitization, validation and escaping
- Validate and sanitize input on receipt (sanitize functions, type casts, allowlists); unslash input where WordPress requires it.
- Escape on output for the exact context: HTML, attribute, URL, JavaScript, textarea. Use `wp_kses`-style allowlist filtering only when limited HTML is required.
- Do not output unescaped user data, option values or database content. Escape late, at the point of output.

## Database access
- Use `$wpdb->prepare()` for any query containing variable data; never concatenate untrusted data into SQL. Prefer `WP_Query`, `get_posts`, meta and options APIs over raw SQL when they suffice.
- Use the `$wpdb` table prefix property rather than hard-coded `wp_`. Do not alter core tables.
- Custom tables: create and upgrade them through a versioned upgrade routine (for example using the schema upgrade helper), store a schema version option, and keep upgrades idempotent and backward compatible. Never run destructive schema changes or production data changes without approval and a backup plan.

## File uploads and media
- Use the WordPress upload and media APIs for handling uploads. Restrict allowed MIME types and extensions, check capability and nonce, and never trust client-reported file types.
- Do not store uploads in executable locations or permit executable file types. Authorize access to private files.

## REST API
- Every registered route needs an explicit permission callback. Do not use a permissive callback for non-public data.
- Validate and sanitize arguments through the route argument definitions. Return appropriate status codes and avoid leaking internal data.
- Cookie-authenticated REST requests require the REST nonce. Use Application Passwords or another supported mechanism for non-browser clients, over HTTPS only.

## Authentication, cookies and sessions
- Use WordPress's authentication, user and cookie APIs. Do not build custom login, password hashing or session handling unless approved.
- Do not use PHP native sessions in a way that breaks caching or REST; verify hosting behavior first.
- Never log or expose auth cookies, nonces, application passwords or keys. Keep salts and keys outside source control.

## Compatibility and dependencies
- Declare and test minimum WordPress and PHP versions supported by the project. Avoid deprecated functions.
- Avoid conflicts with other plugins and themes: namespace, prefix, and avoid global state changes.
- Use Composer or npm only if the project already does; review license, maintenance and vulnerabilities before adding a dependency, and do not bundle libraries that are already provided by core.

## Testing and debugging
- Use the project's configured test tools only. Do not invent commands. If none exist, state this and propose a minimal approach for approval.
- Test capability and nonce failures, validation, escaping of hostile input, REST permission behavior and upgrade routines using an isolated test site and database, never production.
- Use debug logging only in non-production, keep debug display off in production, and never commit debug output or secrets.

## Performance and caching
- Avoid unbounded queries, queries in loops and expensive work on every request. Paginate and limit queries.
- Use object cache and transients only with defined expiry and invalidation. Account for sites with and without persistent object caching.
- Load assets conditionally. Measure before optimizing.

## Deployment and maintenance
- Keep core, themes and plugins updated according to project policy; review changelogs and security advisories.
- Disable file editing in production where policy requires, restrict file permissions, and use HTTPS.
- Keep environment configuration and secrets out of source control. Back up and verify restore before schema, plugin or core changes in production. Production deployment requires explicit approval.
