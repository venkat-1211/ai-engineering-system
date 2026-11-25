# Performance, Scalability and Production Readiness Standard

- Measure before optimizing. Define a baseline and measurable acceptance criteria such as latency, throughput, error rate or resource use.
- Avoid repeated work, unnecessary DB/network round trips and unbounded collections.
- Paginate or stream large data. Bound concurrency and resource consumption.
- Cache only with understood freshness, invalidation and consistency behavior.
- Move long work to background processing where appropriate; avoid blocking request workers/event loops.
- Set timeouts and cancellation for external calls. Retry only safe operations with bounded policies and idempotency.
- Index from actual query patterns and inspect query plans. Monitor locks, pools, slow queries and storage.
- Define graceful shutdown, health/readiness, backup/restore and recovery expectations appropriate to the service.
- Separate dev/staging/production configuration. Protect secrets and use least-privilege identities/network access.
- Disable debug modes and verbose errors in production. Log structured events with correlation IDs and redact sensitive values.
- Monitor errors, latency, saturation, queue depth and critical business events where infrastructure supports it.
- Plan deployment and schema compatibility. Require approval for production deployment, destructive changes and external side effects.
- Never invent capacity, uptime, throughput or cost claims. State assumptions and request load data when necessary.
