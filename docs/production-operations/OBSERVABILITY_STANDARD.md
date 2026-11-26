# Observability Standard

## Three core signals
- Logs explain discrete events and diagnostic context.
- Metrics quantify behavior over time.
- Traces connect work across service boundaries.

Use the signals appropriate to the architecture; do not add instrumentation without a clear operational question.

## Logging
Use structured, timestamped logs with consistent severity and correlation identifiers. Record actionable context while minimizing sensitive data. Never log passwords, access tokens, private keys, full payment credentials or unnecessary personal data. Define retention, access and deletion controls.

## Metrics
Prefer bounded-cardinality labels. Monitor traffic, errors, latency and saturation where meaningful. Define units, aggregation windows and ownership. Avoid user identifiers, raw URLs with secrets or unbounded labels.

## Tracing
Propagate trace and correlation context across supported service boundaries. Sample deliberately and assess cost, privacy and data residency implications.

## Dashboards
Dashboards should answer: Is the service available? Are users affected? What changed? Which dependency is unhealthy? Is capacity approaching a limit? Include time ranges, units, ownership and links to runbooks.

## Alerts
Alert on actionable symptoms and user impact, not every unusual metric. Every paging alert needs severity, owner, response expectation, runbook and a tested notification route. Remove noisy or unactionable alerts.

## Verification
Prove telemetry is emitted, retained, searchable and access-controlled. A configuration file or dashboard screenshot alone does not prove end-to-end alert delivery.
