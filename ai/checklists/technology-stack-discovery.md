# Technology Stack Discovery Checklist

Not every project has every file below. Inspect only what exists and record anything unavailable as **unknown**.

- [ ] Read root `AGENTS.md`.
- [ ] Inspect repository structure and Git status (if not a Git repository, report it; do not initialize Git).
- [ ] Inspect manifests and lockfiles (for example Composer, npm/pnpm/yarn, Python or Java manifests) where present.
- [ ] Identify languages and verified versions.
- [ ] Identify frameworks and verified versions.
- [ ] Identify CMS platforms (for example WordPress, OJS) from installed code, headers or configuration, and their verified versions.
- [ ] Identify runtime and package manager.
- [ ] Identify frontend/backend boundaries and deployment boundaries (same origin, separate origins/hosts, proxies).
- [ ] Identify authentication and authorization architecture (sessions, cookies, tokens, roles, policies, tenant boundaries).
- [ ] Identify databases, drivers and migration tools; inspect database migrations and schema where present (excluding secrets).
- [ ] Identify API, queue, cache and external integration boundaries.
- [ ] Inspect Docker/container and CI/CD configuration where present.
- [ ] Identify test, lint, format, type-check and build commands that are actually configured.
- [ ] Identify deployment configuration.
- [ ] Read the applicable standards under `docs/technology/` (only those that match the detected stack, per `docs/technology/README.md`).
- [ ] Record unknowns rather than guessing.
- [ ] Identify conflicts with approved project conventions.
- [ ] Confirm whether clarification or approval is required.
