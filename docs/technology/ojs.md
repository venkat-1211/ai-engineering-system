# OJS (Open Journal Systems) Engineering Standard

Apply only when OJS is present (for example an OJS installation, an OJS plugin or an OJS theme plugin). Use together with `core-php.md`, `mysql.md`, `javascript-typescript.md` and `html-css-bootstrap-responsive-ui.md` where those technologies are present. Do not apply Laravel, WordPress or other framework architecture to OJS.

This standard does not document OJS APIs. Do not invent classes, hooks, methods, template variables or file locations.

## Mandatory discovery before using OJS-specific APIs
- Identify the exact OJS version from the installed code or configuration, plus the PHP and database versions.
- Inspect the installed OJS code, the existing theme or plugin, its version file/metadata and its registered extension points. Base all API use on what exists in the installed version.
- Check for existing parent theme, child theme, locale files, template files and overrides before adding anything.
- If a needed API cannot be confirmed in the installed code or official documentation for that version, stop and ask rather than guess.

## Architecture and extension conventions
- Extend OJS through its plugin system and documented extension points rather than modifying core files. Do not edit core.
- Follow the existing plugin category, directory layout, naming and registration approach used by the installed version and the project.
- Follow the plugin lifecycle as implemented in the installed version (registration, enablement, settings, upgrades, removal). Make lifecycle code idempotent and avoid destructive removal of data without approval.

## Theme plugin development
- Verify how the installed version defines and registers theme plugins and how it handles theme options, stylesheets and scripts. Follow the existing theme.
- Respect theme inheritance: use a child theme or override only the templates and assets that must change. Do not copy the whole parent theme.
- Customization boundaries: keep presentation changes in the theme; do not put business logic, permissions or database changes in a theme.

## Templates and Smarty
- OJS templates use Smarty where the installed version does. Follow the existing template, block and variable conventions found in the code.
- Escape output for its context using the template escaping mechanisms the installed version provides; do not output unescaped user, submission or metadata content. Verify the default escaping behavior of the installed version.
- Keep logic out of templates; do not call undocumented or unverified template functions.

## Hooks and extension points
- Discover available hooks from the installed code and existing plugins. Register only hooks that exist and use their documented argument and return behavior.
- Document each hook used, avoid expensive work in frequently called hooks, and avoid unintended interaction with other plugins.

## Safe PHP, validation and escaping
- Apply `core-php.md`. Treat all request data, uploaded files and imported metadata as untrusted.
- Validate input on the server using the project's existing validation approach; encode output for HTML, attributes, URLs and JavaScript contexts.
- Do not use direct superglobals or raw SQL when the existing code uses OJS-provided abstractions; follow the established pattern after inspecting it.

## Authorization and roles
- Enforce role and permission checks server-side using the mechanisms the installed version provides. Check journal/context scoping and submission or object-level access.
- Never rely on hidden menu items or template conditions as authorization. Never trust client-supplied role, context, user or submission identifiers.
- Do not weaken access to unpublished submissions, reviews, reviewer identity, author data or editorial decisions.

## Database access and schema safety
- Use the data access approach already used by the installed version and plugin. Use parameterized queries only; never concatenate untrusted data into SQL.
- Do not change core tables or schema. Plugin schema changes require a versioned, idempotent, backward-compatible upgrade routine, a backup and recovery plan, and approval.
- Never run destructive database operations or production data changes without explicit approval.

## Version compatibility and upgrades
- Declare the OJS versions supported. Do not use APIs removed or deprecated in the installed version; verify behavior across the supported range if more than one version is targeted.
- Keep customizations upgrade-safe: minimal overrides, no core edits, documented extension points, and a note of anything that must be re-checked after an OJS upgrade.

## Frontend assets
- Register and load CSS and JavaScript through the installed version's asset mechanism, as the existing theme does. Do not hard-code script tags or add a second UI framework without approval.
- Verify the bundled UI framework and versions before using version-specific classes. Follow the build tooling already present; do not invent build commands.

## Responsive design and accessibility
- Apply `html-css-bootstrap-responsive-ui.md`. Test narrow mobile through desktop viewports and keyboard access, visible focus, contrast, labels, alt text and reflow.
- Maintain accessibility of article pages, issue listings, search, forms and galleys. Claim visual verification only if actually performed in a browser.

## Separation of UI and backend changes
- Keep UI-only changes (templates, CSS, JavaScript, theme options) separate from backend, plugin logic and database changes, in separate reviewable steps.
- Do not combine a theme change with a schema or permission change without explicit approval and a clear plan.

## Testing and debugging
- Use only test and build tooling found in the repository. Do not invent commands; if none exist, say so.
- Test with a non-production OJS instance and database. Cover validation, escaping of hostile metadata, role and context authorization, upgrade routines and template rendering in the supported browsers.
- Keep debug output and verbose errors off in production. Do not expose configuration, secrets or reviewer-identifying information in logs.

## Performance and security
- Avoid expensive queries or work in templates and frequently called hooks; paginate large listings; use caching only with understood invalidation after verifying what the installed version already caches.
- Protect secrets and configuration, keep uploads non-executable and access-controlled, use HTTPS, and review dependencies before adding them.
- Production deployment, upgrades and data changes require explicit approval.
