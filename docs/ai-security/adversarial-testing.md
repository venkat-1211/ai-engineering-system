# Adversarial Testing

Derive tests from the threat model and cover both model behavior and deterministic enforcement. Test direct/indirect prompt injection, secret/context disclosure, cross-tenant retrieval/cache/conversation isolation, unauthorized tools, scope expansion, privilege escalation, malformed arguments, path traversal/SSRF/injection where applicable, unsafe output handling, rate-limit bypass, replay, resource exhaustion, malicious files, poisoned retrieval, compromised dependencies, and fail-closed behavior. Use authorized isolated environments and synthetic/approved data; never test third parties without permission. Record test ID, threat, preconditions, exact commit/configuration/environment, expected and observed results, evidence, severity, and regression status. Unexecuted tests are NOT RUN.

## Mandatory engineering principles
- Treat user input, retrieved content, uploaded files, tool output, and model output as untrusted until validated.
- Untrusted content never overrides trusted policy or grants permissions.
- Model-generated intent is not authorization; enforce authorization server-side at execution time.
- Apply least privilege and deny-by-default permissions to users, agents, tools, services, data, and environments.
- Validate structured arguments, resource identifiers, destinations, paths, payload sizes, rates, and execution time.
- Require human approval for high-impact, irreversible, privileged, financial, or externally visible actions according to approved policy.
- Minimize and protect personal/confidential data; isolate tenants and projects.
- Keep secrets out of prompts, source control, logs, fixtures, and generated artifacts.
- Isolate untrusted code and files with actual OS/container/VM/network controls; prompts are not a sandbox.
- Review dependencies, model/provider integrations, tools, and artifacts according to risk.
- Use authorized environments and synthetic or explicitly approved test data.
- Never mark unexecuted tests PASS or silently suppress security findings.
- Accepted risks require a named human owner, scope, rationale, compensating controls, approval, and expiry.
- Agents cannot approve their own exceptions, access expansions, or high-impact releases.
