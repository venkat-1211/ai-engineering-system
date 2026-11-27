# Quality Evidence and Release Gates

## Evidence record
For each material verification activity capture:
- Change identifier and commit SHA
- Test scope and linked acceptance criteria/risks
- Environment, versions, configuration, and data profile
- Exact command or procedure
- Status using the standard vocabulary
- Relevant output, artifact, or report reference
- Failures, skipped checks, deviations, and limitations
- Reviewer/owner and approval reference where required

## Release decision
Evaluate required checks, unresolved defects, security findings, operational readiness, rollback strategy, and residual risk. A green pipeline is one input, not the whole decision.

## Exceptions
Any exception must identify the requirement waived, reason, risk, compensating control, owner, approver, expiry, and review date. Agents cannot approve their own exceptions.

## Honest claims
State only what evidence supports. Scope claims to the exact commit, configuration, environment, and checks. Explicitly list `Not run`, `Blocked`, and `Requires human approval` items.

## Handoff
Provide a concise quality summary with links to evidence and open issues. Do not describe a release as fully verified if material checks remain outstanding.
