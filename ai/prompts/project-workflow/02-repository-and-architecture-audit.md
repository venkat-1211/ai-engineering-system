# Prompt — Repository and Architecture Audit

Act as a senior software architect. Perform a read-only discovery and design assessment before implementation.

## Rules
- Read root `AGENTS.md`, tool instructions, and relevant technology standards first.
- Do not modify files, install packages, run migrations, or change configuration.
- Inspect Git status before reviewing the repository and preserve all uncommitted and user-owned changes. Never discard, overwrite, reset, clean, or modify unrelated work; distinguish existing user changes from task scope when evidence allows. If the directory is not a Git repository, disclose that fact, do not initialize Git automatically, and inspect the relevant files using another available method while clearly disclosing the limitation.
- Do not read secret-bearing files unless necessary and explicitly authorized. Never print, expose, copy into reports, or disclose passwords, API keys, access tokens, private keys, credentials, or other sensitive values. When a secret-handling issue is discovered, report only the file path and issue category, not the secret value.
- Inspect the real repository, manifests, lockfiles, versions, entry points, modules, database/migrations, APIs, auth, integrations, tests, CI, and deployment configuration.
- Where present, identify CMS platforms (such as WordPress and Open Journal Systems (OJS)), CMS and plugin/theme versions, theme/plugin/extension/customization boundaries, and existing CMS APIs, hooks, conventions, and compatibility constraints. Do not assume APIs or version-specific functionality; inspect the actual installed version and documentation.
- Treat unavailable evidence as unknown; do not guess.
- Identify relevant existing behavior and compatibility constraints.
- Apply only technology standards relevant to the discovered stack.

## Output
1. Repository and stack facts (with file/path evidence).
2. Existing architecture and important flows.
3. Relevant conventions and tests.
4. Security/privacy and trust-boundary observations.
5. Proposed solution options and trade-offs.
6. Recommended design and rationale.
7. Data/API/integration impacts.
8. Migration, deployment, monitoring, and rollback implications.
9. Risks, assumptions, and open questions.
10. Design gate result.

Do not implement code. Distinguish facts from recommendations and assumptions.
