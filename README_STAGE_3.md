# Stage 3 — Technology-Specific Engineering Standards

Stage 3 adds conditional engineering standards for common technology stacks. It is an add-on to Stages 1 and 2, not a replacement for their supporting files.

## Install
1. Commit or back up your current repository.
2. Extract this package into a temporary folder, not over your repository.
3. Keep all Stage 1 and Stage 2 files unless a later stage explicitly replaces them.
4. Copy the Stage 3 `docs/technology/` files into the matching folder. Merge the Stage 3 files in `ai/checklists/` and `ai/prompts/` into the matching folders, reviewing any file that already exists before overwriting it.
5. **Merge, do not replace, the root `AGENTS.md`.** Keep a single root `AGENTS.md` and do not create a second one. Preserve your existing project-specific instructions, and add only the Stage 3 additions:
   - In the section that selects standards (Section 3, "Discover the stack and select standards"), add the list of technology standards (see below) and the instruction to select only applicable standards.
   - In the context-reading section (Section 2), add the instruction to read `docs/technology/README.md` and only the standards relevant to the detected stack.
   - In the precedence section (Section 1), add `docs/technology/` standards after `AGENTS.md` and before tool-specific adapters.
   - If your `AGENTS.md` already contains equivalent text, do not duplicate it; resolve any conflict explicitly.
6. Review the combined changes and commit them.

## Included standards (13)
All files are in `docs/technology/`, with a selection guide in `docs/technology/README.md`.

| Standard | File |
|---|---|
| Core PHP | `core-php.md` |
| Laravel | `laravel.md` |
| WordPress | `wordpress.md` |
| OJS (Open Journal Systems) | `ojs.md` |
| JavaScript/TypeScript | `javascript-typescript.md` |
| React | `react.md` |
| Node.js/Express | `nodejs-express.md` |
| MySQL and relational databases | `mysql.md` |
| MongoDB | `mongodb.md` |
| HTML/CSS/Bootstrap/responsive UI | `html-css-bootstrap-responsive-ui.md` |
| REST APIs and integrations | `rest-apis-integrations.md` |
| Testing and automation | `testing-automation.md` |
| Performance, scalability and production readiness | `performance-scalability-production.md` |

## Additional Stage 3 improvements
- **PHP session and cookie security:** `core-php.md` covers session fixation, ID regeneration, secure cookie attributes, lifetime, CSRF and safe logout.
- **Laravel SPA authentication and CORS:** `laravel.md` covers cookie-based SPA authentication, stateful domains, explicit CORS origins and credentialed requests, CSRF and cookie configuration, and token authentication only where justified. A wildcard origin must not be combined with credentialed browser requests.
- **Git-unavailable handling:** `ai/prompts/technology-stack-audit.md` and `ai/prompts/technology-aware-task.md` tell agents to report clearly when the workspace is not a Git repository, never to initialize Git automatically, and not to claim a Git diff was reviewed.
- **Production-readiness verification statuses:** `ai/checklists/production-readiness.md` and `ai/checklists/TASK_COMPLETION_CHECKLIST.md` report each check as Passed, Failed, Not run, Blocked or Requires human approval, with evidence.
- **Discovery checklist:** `ai/checklists/technology-stack-discovery.md` also covers CMS platforms, deployment boundaries, authentication architecture, migrations, Docker and CI.

## Required behavior
Agents must discover the actual stack from repository evidence, verify versions, select only relevant standards, follow approved project conventions, and disclose unknowns. CMS standards (WordPress, OJS) are independent of framework standards and require verifying the installed version and existing code before using CMS-specific APIs. These standards do not themselves enforce permissions or runtime behavior.

## First use
Run `ai/prompts/technology-stack-audit.md` as a read-only audit. Use `ai/prompts/technology-aware-task.md` for implementation tasks.
