# Post-Deployment Verification

Verification should be independent of the deployment command's exit code.

Minimum checks as applicable:
- Correct environment, version, commit, and artifact digest are running.
- Readiness and liveness/health endpoints pass.
- Critical smoke tests and representative user journeys pass.
- Database migrations and background workers are healthy.
- Error rates, latency, saturation, queue depth, and key business metrics remain within defined thresholds.
- Security controls, access boundaries, and scheduled jobs remain effective.
- Logs and traces show no unexpected failure patterns.
- Rollout/traffic distribution matches the intended strategy.

Record exact checks, timestamps, environment, evidence, deviations, and human acceptance. If a check was not executed, mark `Not run`, not `Passed`.
