# Release Gates & Evidence

## Required go/no-go checks
- Change scope, owner, risk, and affected services are known.
- Required reviews and approvals are recorded.
- Tests and quality checks meet Stage 9 policy.
- Security, dependency, secret, and supply-chain checks meet Stage 10 policy.
- Artifact is immutable, traceable, integrity-checked, and built from the intended commit.
- Environment configuration and permissions are validated.
- Database/data migration plan and backup/recovery evidence are adequate.
- Monitoring, health checks, and post-deployment verification are ready.
- Rollback or forward-recovery plan is viable.
- Production approval is explicit and human-owned.

## Evidence record
Record repository, commit, branch/tag, pipeline run, tool versions, artifact digest, environment, test/security outcomes, approvals, migration result, deployment result, verification, exceptions, and final decision.

## Decision
`GO` only when all mandatory controls pass and authorized human approval is present. Otherwise `NO-GO` or `Requires human approval`. A waiver must follow Stage 6 and cannot waive legal, security, or platform constraints that are non-waivable.
