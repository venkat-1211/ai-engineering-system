# 06 — Integrate Stage 10 and Independent Read-Only Audit

## Baseline
Confirm repository root, branch, HEAD, and Git status. Inspect root `AGENTS.md`, root README, and Stages 1–9. Identify actual conventions and conflicts.

## Package review
Verify all 33 expected files exist and are readable/non-empty. Review every document, template, checklist, and prompt. Correct only confirmed Stage 10 defects. Preserve previous stages.

## Integration
Integrate `AGENTS_STAGE_10_ADDENDUM.md` into the existing root `AGENTS.md`. Never replace/truncate it or reorder unrelated sections. Preserve Stages 1–9. Add concise enforceable rules and links. Mark addendum `(Merged)` only after verification. Preserve root README.

## Cross-stage validation
Check duplicate authority, broken links, conflicting approvals, contradictory test labels, and weakened controls across Stages 1–10. Apply stricter applicable controls; report unresolved conflicts.

## Independent read-only audit
Freshly verify all paths/content, root AGENTS integration, prior-stage preservation, all mandatory security invariants, threat modeling, prompt injection, least privilege, server-side authorization, data protection, secrets, sandboxing, supply chain, adversarial tests, findings, incident response, release gates, internal links, Git diff/status, and whitespace.

## Restrictions
Do not stage, commit, push, amend, install packages, run destructive/privileged/external/production-impacting actions, access or print secret values, or modify Stages 1–9. Separate integration changes from audit actions.

## Report
Provide verdict PASS / PASS WITH FINDINGS / FAIL; repository path/branch/HEAD; exact file counts; changed AGENTS sections and preservation evidence; mandatory-rule table with file/line evidence; cross-stage compatibility; link/whitespace checks; Git status/diff; findings with severity/evidence; tests/scans not run and limitations; and READY TO COMMIT / NOT READY TO COMMIT. Stop without committing or pushing.
