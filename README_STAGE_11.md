# Stage 11 — DevOps, CI/CD & Release Engineering

## Purpose
Establish secure, repeatable, observable, and recoverable delivery practices across projects and technology stacks. These standards govern source control, build pipelines, deployment, environment configuration, infrastructure changes, release approvals, rollback, and post-deployment verification.

## Scope
- Git collaboration and release branching
- CI pipeline design and quality gates
- Build, package, artifact provenance, and versioning
- CD deployment strategies and environment promotion
- Configuration, secrets, and environment separation
- Infrastructure as Code (IaC) and change control
- Pipeline identity, permissions, and supply-chain security
- Release readiness, approvals, rollback, and recovery
- Deployment observability and post-release verification

## Required operating principles
1. Automate repeatable delivery steps; retain human approval for production and other high-impact changes.
2. Build once and promote the same immutable artifact through environments.
3. Never store secrets in source control, logs, artifacts, prompts, or pipeline output.
4. Apply least privilege to runners, deployment identities, service connections, and cloud roles.
5. Treat pipeline definitions and IaC as production code: review, test, version, and audit them.
6. Make deployments traceable to source commit, build, artifact digest, approvals, and deployment record.
7. Every production release must have a tested recovery or rollback approach appropriate to the change.
8. A successful pipeline is evidence only for the checks it actually executed.
9. Keep development, test, staging, and production data and credentials appropriately separated.
10. Do not claim a deployment succeeded until the target environment has been independently verified.

## Repository integration
- Merge `AGENTS_STAGE_11_ADDENDUM.md` into the existing root `AGENTS.md`; do not replace the existing file.
- Preserve all prior stage instructions and section ordering.
- Keep this package's source files under their supplied paths.
- Resolve cross-stage conflicts by preserving stricter existing safety and human-approval requirements.

## Suggested adoption sequence
1. Inventory current repositories, environments, pipelines, runners, credentials, and deployment paths.
2. Classify services and release risk.
3. Define branch, build, artifact, promotion, approval, and rollback conventions.
4. Implement a minimum secure CI pipeline.
5. Add deployment automation and environment verification.
6. Validate recovery procedures in a safe environment.
7. Capture evidence and obtain human acceptance before production adoption.

## Evidence and status language
Use only: `Passed`, `Failed`, `Not run`, `Blocked`, `Requires human approval`.
Do not mark a control or test as passed without evidence. Record scope, commit, environment, timestamp, tool/version, result, and evidence location where applicable.

## Stage 11 file map
See `docs/devops-release/README.md` for the complete standards index.
