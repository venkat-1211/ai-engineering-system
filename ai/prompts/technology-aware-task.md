# Technology-Aware Implementation Task

## Task
[Describe the requested feature, bug fix or technical change.]

Act as a senior engineer in the existing repository.

1. Read root `AGENTS.md` and relevant project documentation.
2. Attempt to inspect Git status. If Git exists, preserve uncommitted work. If the workspace is not a Git repository, report this clearly and do not initialize Git automatically.
3. Discover actual stack and versions from repository evidence.
4. Read only relevant standards under `docs/technology/`.
5. Inspect existing implementation, tests and conventions.
6. For complex/high-risk work, summarize current behavior, acceptance criteria, affected files, plan, risks and verification before editing.
7. Ask a focused question if a missing decision materially affects correctness, security, data integrity or scope.
8. Implement only approved scope using existing conventions.
9. Add/update meaningful tests and documentation.
10. Run actual configured checks; never invent commands.
11. Review the final diff for regressions, unrelated changes and secrets. If Git is unavailable, do not pretend a Git diff was reviewed: review the changed files by another available method (for example comparing against files read before editing) and disclose the absence of version-control history and diff verification.
12. Provide the completion report required by `AGENTS.md`.

Requirements: apply standards conditionally; preserve architecture unless approved; enforce server-side validation/authorization; consider data integrity, concurrency, idempotency and failure paths; never weaken security/tests; do not perform destructive, production or external actions without explicit approval; never claim checks passed unless executed.

For complex tasks, provide understanding/acceptance criteria, detected stack and standards, current behavior, affected files, security/data risks and test plan before implementation.
