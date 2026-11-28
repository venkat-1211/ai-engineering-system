# Authentication Authorization

Separate human, workload, agent, and service identities. Verify identity at service boundaries; a model statement is not authentication. Deny by default; grant least privilege; enforce role/attribute and resource-level policies server-side; derive tenant/ownership scope from authenticated context; re-check authorization for asynchronous jobs and tool calls; separate read/write/export/admin/destructive capabilities; use short-lived scoped tokens and revoke promptly. Fail closed for protected actions if identity or policy services are unavailable. Test horizontal/vertical escalation, cross-tenant access, stale sessions, revoked tokens, and confused-deputy paths.

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
