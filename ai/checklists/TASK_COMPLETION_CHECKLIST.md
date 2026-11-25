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
- [ ] Relevant automated tests were executed.
- [ ] Negative and edge cases were tested.
- [ ] Static analysis/lint/format/build checks were run where available.
- [ ] Regression risks were checked.
- [ ] Unrun checks and reasons are disclosed.

## Handoff
- [ ] Final diff was inspected.
- [ ] Documentation was updated where necessary.
- [ ] Files changed are listed.
- [ ] Known limitations and residual risks are listed.
- [ ] Human approvals still required are identified.

**Do not mark unchecked items as complete. Explain items that do not apply.**
