# Incident Response

Triggers include suspected data exfiltration, unauthorized tool execution, compromised credentials, cross-tenant exposure, malicious dependency/model update, agent runaway, or policy bypass. Sequence: detect/declare; contain safely (disable tools, revoke tokens, isolate workload); preserve logs/request IDs/timestamps/config/commit without copying secrets; determine identities, tenants, data, tools, providers, time window, downstream actions; eradicate and rotate/revoke; recover with heightened monitoring; notify stakeholders under approved procedures; conduct blameless review and add regression tests/monitoring/owners. Do not destroy evidence or make unsupported impact/notification claims. Escalate to human incident commander.

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
