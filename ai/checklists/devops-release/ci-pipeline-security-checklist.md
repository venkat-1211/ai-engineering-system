# CI Pipeline Security Checklist

- [ ] Pipeline definitions are reviewed and protected.
- [ ] Runner is isolated and appropriately ephemeral.
- [ ] Job permissions are minimal.
- [ ] Untrusted code has no privileged secrets or deployment access.
- [ ] Dependencies/actions/images are pinned and provenance reviewed.
- [ ] Secrets use approved stores and are never printed.
- [ ] Caches and artifacts are protected from poisoning/tampering.
- [ ] Network egress is restricted where feasible.
- [ ] Required security and quality checks fail closed.
- [ ] Pipeline logs and retention meet policy.
- [ ] Exceptions are approved and time-bounded.

Status: `Passed` / `Failed` / `Not run` / `Blocked` / `Requires human approval`
Reviewer:
Evidence:
