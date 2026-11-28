# Prompt 06 — Independent Read-Only Stage 11 Audit

Act as an independent auditor. Do not edit files, install dependencies, change permissions, run deployment/IaC apply commands, stage, commit, amend, or push.

Audit:
- All expected Stage 11 files and non-empty contents.
- Root `AGENTS.md` integration preserves all previous stages and sections.
- Root README and Stages 1–10 remain unchanged except explicitly authorized integration.
- Cross-stage consistency with Stages 4, 6, 7, 9, and 10.
- Branch/CI/CD/artifact/environment/secrets/IaC/release/migration/recovery/post-deploy controls.
- Human approval gates and agent restrictions.
- Internal links, exact paths, duplicate headings, placeholders, conflict markers, trailing whitespace, and `git diff --check`.
- Git status, staged/unstaged/untracked scope, and unexpected files.

Use evidence with exact paths and line/section references. Separate documentation checks from actual pipeline/deployment execution. Do not claim real infrastructure or CI controls were tested if this documentation-only repository cannot verify them.

Return `PASS — READY TO COMMIT` only if all package files and integration requirements are satisfied, no unresolved findings remain, and the intended change scope is exact. Otherwise return `FAIL — FIX REQUIRED` with actionable findings. Leave Git untouched.
