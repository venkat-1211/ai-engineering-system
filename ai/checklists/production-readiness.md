# Production Readiness Checklist

Apply relevant items and explain exclusions.

## Correctness and data
- [ ] Acceptance criteria are explicit and met.
- [ ] Validation and error paths are handled.
- [ ] Data integrity and transaction boundaries are considered.
- [ ] Concurrency, retries and duplicate requests are considered.
- [ ] Migrations fit the deployment plan.
- [ ] Backup/recovery impact is understood for data changes.

## Security
- [ ] Authentication and server-side authorization are enforced.
- [ ] Tenant/ownership isolation is tested where relevant.
- [ ] Secrets and sensitive data are protected.
- [ ] Inputs and outputs are handled safely.
- [ ] Rate limits and abuse controls are considered.
- [ ] Dependencies/configuration are reviewed.
- [ ] Logs and errors do not disclose sensitive data.

## Reliability and operations
- [ ] Timeouts and failure behavior are defined.
- [ ] Retries are bounded and safe.
- [ ] Monitoring and health checks are considered.
- [ ] Performance is measured where required.
- [ ] Deployment and rollback/forward-recovery plan is understood.
- [ ] Human approval exists for production or irreversible actions.

## Verification
- [ ] Relevant automated tests were actually executed and passed (record the exact command and result).
- [ ] Static analysis/type checks/lint/build were actually executed and passed where configured.
- [ ] Critical workflows are checked.
- [ ] Final diff is reviewed (or, if Git is unavailable, changed files were reviewed by another method and this is disclosed).
- [ ] Unrun checks and residual risks are disclosed.

## Verification status reporting
Report every check under exactly one status, with evidence (command, output summary or reason):

| Status | Meaning |
|---|---|
| Passed | The check was executed and succeeded; evidence recorded. |
| Failed | The check was executed and failed; failure details recorded. |
| Not run | The check was not executed; reason stated. |
| Blocked | The check could not run (for example missing tooling, network or sandbox restriction); blocker stated. |
| Requires human approval | The check or action needs explicit approval before running (for example destructive, production or paid operations). |

Never report an implementation as verified without evidence. Not-run, blocked and approval-pending checks must not be described as passed.
