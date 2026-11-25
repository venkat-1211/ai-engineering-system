# Technology Standards — Selection Guide

These standards are conditional. Apply only those relevant to the actual project.

1. Inspect manifests, lockfiles, source, configuration, migrations, CI and deployment files.
2. Record only versions that can be verified; mark unknown versions explicitly.
3. Identify runtime, package manager, frontend/backend boundaries, databases, APIs and test tooling.
4. Select relevant standards below.
5. Follow approved project architecture where safe; do not introduce a new architecture merely because a standard describes it.
6. Explain conflicts before material changes.

| Standard | Apply when |
|---|---|
| `core-php.md` | PHP exists |
| `laravel.md` | Laravel exists |
| `wordpress.md` | WordPress exists (themes, plugins or configuration) |
| `ojs.md` | OJS exists (installation, plugins or theme plugins) |
| `javascript-typescript.md` | JavaScript/TypeScript exists |
| `react.md` | React exists |
| `nodejs-express.md` | Node.js/Express exists |
| `mysql.md` | MySQL or relational DB exists |
| `mongodb.md` | MongoDB exists |
| `html-css-bootstrap-responsive-ui.md` | Browser UI exists |
| `rest-apis-integrations.md` | APIs, webhooks or external services exist |
| `testing-automation.md` | Any application is tested |
| `performance-scalability-production.md` | Production/performance concerns apply |

## Selection rules
- Select only the standards that apply to the detected stack.
- Multiple standards may apply to one project; apply them together and resolve overlaps in favor of the more specific standard and the existing approved design.
- CMS standards (`wordpress.md`, `ojs.md`) are independent of framework standards: do not apply `laravel.md` to WordPress or OJS, and do not apply WordPress or OJS conventions to other projects. `core-php.md` still applies to PHP code in a CMS, but the CMS standard's conventions and APIs take precedence over generic PHP structure where they differ, and generic session handling in `core-php.md` applies only to hand-written session code.
- CMS-specific APIs must be verified against the installed version and existing code before use.
- Do not force unrelated frameworks or architectures into a project.

Examples: Laravel + MySQL uses Core PHP, Laravel, MySQL, Testing and API standards if applicable. React + Express + MongoDB uses JavaScript/TypeScript, React, Node.js/Express, MongoDB, API and Testing standards. A WordPress theme uses WordPress, Core PHP, JavaScript/TypeScript and HTML/CSS standards, plus MySQL if it touches the database. An OJS theme uses OJS, Core PHP, JavaScript/TypeScript and HTML/CSS standards. A React frontend with a Laravel backend uses React, JavaScript/TypeScript, Core PHP, Laravel, API and Testing standards (plus MySQL if applicable).

These documents do not replace version-matched official documentation, security advisories, project requirements or code review.
