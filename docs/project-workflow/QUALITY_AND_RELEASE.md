# Quality, Verification, and Release

## 1. Verification strategy

Derive tests from requirements and risks. Select applicable layers:
- Unit tests for isolated logic and business rules.
- Integration tests for database, queues, storage, and external boundaries.
- Contract tests for API/event compatibility.
- End-to-end tests for critical user journeys.
- Regression tests for existing behavior.
- Security tests for authorization, validation, abuse cases, and sensitive flows.
- Performance/load tests for meaningful capacity or latency risks.
- Accessibility and responsive checks for user interfaces.
- Migration tests and data reconciliation for schema/data changes.

Use realistic test environments where possible. Mocks are useful for isolation but do not replace integration verification of critical boundaries.

## 2. Evidence and status language

Use exactly one status per check:
- **Passed** — executed and succeeded; include command/tool and concise result.
- **Failed** — executed and failed; include relevant error or failing test.
- **Not run** — not executed.
- **Blocked** — could not execute due to a stated blocker.
- **Requires human approval** — action/check requires authorized human decision.

Do not imply complete coverage from a small test suite. State what was and was not checked.

## 3. Defect handling

For each defect, record:
- Reproduction steps and environment.
- Expected versus actual behavior.
- Severity and user/business impact.
- Root cause if known; label hypotheses.
- Fix and regression test.
- Verification result.

Do not suppress, skip, weaken, or delete failing tests merely to obtain a green result without an approved, justified change.

## 4. Release readiness

Before release, review:
- Requirements and scope approval.
- Build and configuration correctness.
- Secrets and permissions.
- Database migrations and data safety.
- Dependency and security findings.
- Test evidence and known defects.
- Performance/reliability risks.
- Backups and recovery.
- Rollback or forward-fix strategy.
- Monitoring, alerts, logs, and support owner.
- Release communication and human approvals.

## 5. Deployment and post-deployment

Use the established deployment mechanism. Prefer staged rollout or feature flags when risk warrants. Do not expose secrets in logs or deployment output.

After deployment, verify:
- Application health and critical endpoints.
- Authentication and authorization.
- Critical business workflows.
- Background jobs and integrations.
- Error rates, latency, resource use, and relevant alerts.
- Migration/data integrity.

If verification fails, follow the approved rollback/recovery plan and notify the responsible owner.

## 6. Operational handoff

Provide relevant runbook information:
- Service purpose and ownership.
- Environments and safe operational commands.
- Configuration dependencies (never secret values).
- Monitoring dashboards and alert meanings.
- Backup/restore and recovery procedure.
- Common failure modes and escalation path.
- Known limitations and follow-up work.
