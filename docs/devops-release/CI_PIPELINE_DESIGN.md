# CI Pipeline Design

## Standard pipeline stages
1. Checkout a specific commit with minimal permissions.
2. Validate formatting, syntax, and repository policy.
3. Resolve dependencies using lockfiles and approved registries.
4. Run unit and component tests.
5. Run integration and contract tests where applicable.
6. Run static analysis, secret scanning, dependency and license checks.
7. Build a deployable artifact.
8. Generate test, security, and build evidence.
9. Publish the artifact only after required gates pass.

## Design rules
- Fail closed for required controls; do not silently skip checks.
- Make stages explicit and results distinguishable (`Passed`, `Failed`, `Not run`, `Blocked`, `Requires human approval`).
- Cache only non-sensitive, integrity-checked data. Do not allow untrusted pull-request code to poison privileged caches.
- Separate untrusted pull-request workflows from privileged release/deployment workflows.
- Use timeouts, concurrency limits, cancellation policy, and resource quotas.
- Keep pipeline logs useful but free of secrets and sensitive payloads.
- Pin pipeline actions/plugins and runner images; update through reviewed changes.
- Avoid broad `continue-on-error` and blanket failure suppression.
- Ensure tests run against the intended commit and report exact scope.

## Failure handling
A failed mandatory gate blocks artifact promotion. Flaky tests must be tracked and fixed; retries do not convert an unresolved failure into a pass.
