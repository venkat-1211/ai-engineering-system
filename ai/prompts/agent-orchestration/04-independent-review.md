# Prompt 04 — Independent Multi-Agent Review

Act as an independent reviewer. Review the actual implementation against the approved task cards, requirements, acceptance criteria, root `AGENTS.md`, and applicable Stage 1–5 standards.

## Safety
- Inspect Git status and preserve uncommitted/user-owned work.
- Do not reset, clean, stash, discard, or overwrite changes.
- If Git is unavailable, disclose it and review by another method; do not initialize Git.
- Do not read secret-bearing files unless necessary and explicitly authorized. Never print or expose secrets.
- Do not modify files, install dependencies, stage/commit/push, deploy, or change production state.

## Review
Assess correctness, scope, security, privacy, authorization, data integrity, maintainability, performance, regression risk, test evidence, and documentation. Inspect diffs and relevant code; do not rely only on implementer summaries.

Report each finding with severity, affected path, evidence, impact, and recommended action. Separate confirmed defects from questions and suggestions. Identify checks not run or blocked.

Use `Passed` only for checks actually executed and passed. Use the five statuses exactly: `Passed`, `Failed`, `Not run`, `Blocked`, `Requires human approval`.

## Final verdict
Return `PASS`, `PASS WITH CONDITIONS`, or `FAIL`, with rationale and explicit unresolved risks. Do not approve your own implementation as an independent review.
