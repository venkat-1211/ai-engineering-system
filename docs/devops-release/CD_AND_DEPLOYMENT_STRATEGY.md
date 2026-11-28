# Continuous Delivery & Deployment Strategy

## Promotion
Promote a previously built immutable artifact through controlled environments. Require environment-specific approvals and policy checks. Production deployment is never inferred from a staging success.

## Strategy selection
- Rolling: suitable when instances can be upgraded incrementally and compatibility is maintained.
- Blue/green: suitable when parallel capacity and rapid traffic switching are available.
- Canary: suitable when gradual exposure and meaningful telemetry exist.
- Recreate/maintenance: use only with accepted downtime and a tested maintenance plan.

## Deployment controls
- Verify target account, project, cluster, region, namespace, and service before execution.
- Use scoped deployment identity and explicit environment selection.
- Define pre-deploy checks, health probes, readiness criteria, timeout, abort threshold, and post-deploy checks.
- Prevent concurrent conflicting deployments and serialize stateful changes.
- Keep deployment output and audit records without exposing secrets.
- Confirm service health and key user journeys after rollout.
- Stop rollout and invoke recovery when defined thresholds are breached.

No deployment is complete until the target environment is verified and the release record is updated.
