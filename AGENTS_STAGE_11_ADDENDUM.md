# Stage 11 Addendum — DevOps, CI/CD & Release Engineering (Merged)

> **Status: Reference-only historical aid (Merged).** Applicable Stage 11 requirements have been selectively integrated into the existing root `AGENTS.md`. Root `AGENTS.md` remains the single active root instruction file; do not replace it or remove any earlier-stage rule. Retain stricter project-specific controls.

## Mandatory delivery rules
- Treat workflows, pipeline YAML, build scripts, deployment scripts, runner images, and IaC as production code subject to review, tests, ownership, and change history.
- Use protected branches and pull-request review for shared and production-bound branches. Do not bypass required checks or branch protections.
- Build from a known commit in a controlled, reproducible environment. Record source revision, toolchain, dependency lock state, artifact identity, and build result.
- Build once; promote the same immutable artifact between environments. Do not rebuild separately for production after staging approval.
- Pin or constrain actions, plugins, container images, and third-party pipeline dependencies. Review provenance and updates.
- Apply least privilege and short-lived identity where supported. Separate build identity from deployment identity and scope each to required resources.
- Never expose credentials in repository files, command arguments, debug traces, artifacts, screenshots, logs, or generated documentation. Use approved secret stores and masked variables.
- Keep environment configuration outside immutable artifacts. Validate required configuration at deployment time without printing secret values.
- Separate environments, credentials, data, and access. Production access and production deployment require explicit human authorization.
- Require approvals for production, destructive infrastructure changes, database migrations with material risk, permission changes, and other high-impact actions.
- Use deployment strategies appropriate to service risk (rolling, blue/green, canary, or controlled maintenance). Define health checks and abort criteria.
- Every production release must have a documented rollback or forward-recovery plan, data compatibility assessment, and accountable owner.
- Database and data migrations must consider backward compatibility, backups, locking, duration, partial failure, and recovery. Do not assume code rollback reverses data changes.
- Verify deployment through independent health, smoke, functional, security, and telemetry checks appropriate to the service.
- Preserve release evidence: approvals, commit, artifact digest, pipeline run, environment, migration outcome, deployment result, verification, and rollback decision.
- Do not claim CI/CD, deployment, backup, rollback, or recovery passed unless it was executed and evidence was reviewed.
- Agents may prepare changes and reports but must not approve production releases, bypass controls, alter access boundaries, or execute high-impact deployments without explicit human authorization.

## Required release gate
A release is blocked when critical checks fail, required evidence is missing, the artifact cannot be traced to source, secrets or permissions are unsafe, production approval is absent, or no viable recovery plan exists. Exceptions require a named human owner, bounded scope, rationale, compensating controls, approval, and expiry under Stage 6 governance.

## Cross-stage integration
Apply Stage 9 test evidence and quality gates, Stage 10 security and supply-chain controls, Stage 7 operations/incident/recovery requirements, Stage 6 exceptions and approvals, and Stage 4 human approval gates. This addendum supplements rather than supersedes them.
