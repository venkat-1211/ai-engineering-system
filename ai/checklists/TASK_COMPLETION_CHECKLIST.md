# AI Task Completion Checklist

Use this checklist before declaring a task complete.

## Scope and requirements
- [ ] The requested problem is understood.
- [ ] Acceptance criteria are explicit and addressed.
- [ ] Assumptions and unresolved questions are disclosed.
- [ ] No unrelated functionality was changed.

## Implementation
- [ ] Existing project conventions were followed.
- [ ] Business logic and validation are in the correct layers.
- [ ] Errors and failure paths are handled.
- [ ] Data integrity and concurrency were considered where relevant.
- [ ] No unnecessary dependencies or abstractions were introduced.

## Security
- [ ] Authentication and authorization were checked.
- [ ] Input validation and output encoding were considered.
- [ ] Sensitive data and secrets are protected.
- [ ] Tenant/ownership boundaries were tested where applicable.
- [ ] Security-sensitive changes received independent review.

## Verification
- [ ] Relevant automated tests were actually executed and passed (record the exact command and result).
- [ ] Negative and edge cases were tested.
- [ ] Static analysis/lint/format/build checks were actually executed and passed where available.
- [ ] Regression risks were checked.
- [ ] Unrun checks and reasons are disclosed.

### Verification status reporting
Report every check under exactly one status, with evidence (command, output summary or reason). This matches `ai/checklists/production-readiness.md`.

| Status | Meaning |
|---|---|
| Passed | The check was executed and succeeded; evidence recorded. |
| Failed | The check was executed and failed; failure details recorded. |
| Not run | The check was not executed; reason stated. |
| Blocked | The check could not run (for example missing tooling, network or sandbox restriction); blocker stated. |
| Requires human approval | The check or action needs explicit approval before running (for example destructive, production or paid operations). |

Tests must actually be executed and pass before they are reported as verified. Never report an implementation as verified without evidence; Not-run, Blocked and approval-pending checks must not be described as passed.

## Handoff
- [ ] Final diff was inspected (or, if Git is unavailable, changed files were reviewed by another method and this is disclosed).
- [ ] Documentation was updated where necessary.
- [ ] Files changed are listed.
- [ ] Known limitations and residual risks are listed.
- [ ] Human approvals still required are identified.

**Do not mark unchecked items as complete. Explain items that do not apply.**
