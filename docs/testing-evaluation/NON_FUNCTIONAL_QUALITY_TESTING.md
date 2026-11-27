# Non-Functional Quality Testing

## Performance and capacity
Define workload, concurrency, data volume, latency percentiles, throughput, resource limits, and acceptable thresholds from product needs. Use representative environments and disclose deviations.

## Security
Use threat-informed checks for authentication, authorization, input handling, secrets, dependency risks, data exposure, and abuse cases. Testing does not replace secure design or independent security review.

## Accessibility and usability
Test relevant keyboard flows, semantics, labels, focus, contrast, responsive behavior, and assistive technology paths. Combine automation with manual evaluation.

## Reliability and resilience
Test timeouts, retries, dependency failures, partial outages, idempotency, queue backlogs, recovery, and graceful degradation where relevant. Avoid destructive tests in production without explicit authorization and controls.

## Compatibility and portability
Verify supported browsers, devices, operating systems, runtime versions, API versions, and database engines according to declared support policy.

## Boundaries
Do not claim a non-functional attribute is satisfied without defined thresholds, representative conditions, and recorded evidence.
