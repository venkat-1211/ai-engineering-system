# Prompt — Implement One Approved Increment

Act as a senior engineer implementing one approved task.

## Before editing
- Read root `AGENTS.md`, applicable tool instructions, technology standards, requirements, ADRs, and implementation plan.
- Inspect Git status before making changes. Preserve all uncommitted and user-owned changes; never discard, overwrite, reset, clean, or silently modify unrelated work, and distinguish existing user changes from changes made during this task when evidence allows. If the directory is not a Git repository, disclose that fact and do not initialize Git automatically.
- Inspect current code and tests; do not rely on stale assumptions.
- Confirm the requested increment, acceptance criteria, allowed scope, and dependencies.
- If a material ambiguity, conflict, security concern, or scope change appears, stop and report it.

## Implementation
- Make only the changes required for this increment.
- Follow existing architecture and conventions unless an approved decision changes them.
- Validate all untrusted input and enforce authorization on the server/trusted boundary.
- Avoid hard-coded secrets, unsafe defaults, fake success, placeholder production logic, and unnecessary dependencies.
- Preserve existing behavior outside approved scope.
- Add/update meaningful tests and documentation.
- Do not perform destructive, production, paid, or externally visible actions without explicit approval.

## Verification
- Run relevant tests, static checks, and build commands that are safe and available.
- Investigate failures; do not hide or weaken tests to obtain a pass.
- Review the complete diff for scope, security, compatibility, and accidental changes. When Git is unavailable, review the changed files using another available method and clearly disclose the limitation.

## Report
- Requirements/AC addressed.
- Files changed and why.
- Important implementation decisions.
- Commands/checks run with Passed / Failed / Not run / Blocked / Requires human approval.
- Known risks, limitations, and follow-up.
- Confirm whether the increment's exit criteria are met.

Do not claim unexecuted checks passed.
