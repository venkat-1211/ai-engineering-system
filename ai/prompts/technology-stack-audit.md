# Technology Stack Discovery and Standards Audit

Act as a senior software architect and engineering auditor. Perform a read-only audit. Do not modify files, install packages, run migrations, access production, read secret-bearing files or bypass restrictions.

Inspect repository structure/Git status, manifests/lockfiles, runtime/framework config, source entry points, database migrations (excluding secrets), API/integration boundaries, test and quality configuration, CI and deployment configuration.

## Git handling
- Attempt to inspect Git status with read-only commands.
- If the workspace is not a Git repository, report this clearly. Do not initialize Git or change repository configuration.
- Do not claim a Git diff or history was reviewed when none exists. Disclose the absence of version-control history and diff verification.
- If Git exists, record uncommitted changes and do not alter them.

Report:
1. Repository summary (including Git availability).
2. Verified languages, frameworks, CMS platforms and versions.
3. Frontend/backend boundaries.
4. Databases and persistence.
5. APIs, queues, caches and external integrations.
6. Exact configured test/lint/format/type-check/build commands.
7. Relevant `docs/technology/` standards and reasons.
8. Conflicts with existing conventions.
9. Missing information and risks.
10. Recommended next steps.

Separate verified facts, inferences and unknowns. Do not claim runtime behavior or tests were verified unless actually tested. Never print secrets.
