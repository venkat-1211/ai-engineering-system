# Agent Tool Security

Use deny-by-default tool allowlists and least-privilege identities. For every call authenticate the caller, authorize the exact operation/resource server-side, validate arguments against strict schemas and business rules, constrain paths/destinations/rates/sizes/timeouts, apply idempotency/replay controls where relevant, and write redacted attributable audit events. Require human approval for high-impact operations such as deletion, publishing, payments, external messaging, permission changes, production deployment, and bulk export. Never trust model-generated user IDs, tenant IDs, roles, paths, SQL, URLs, or approval claims. Avoid unrestricted shell/browser/database/filesystem access.

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
