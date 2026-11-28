# Security Release Gates

Before release verify current threat model, attack-surface/permission inventory, server-side authentication/authorization, applicable prompt-injection and unauthorized-tool tests, data isolation, secrets, output handling, sandboxing, dependency/model/provider/tool review, triaged findings, authorized residual-risk decisions, monitoring, rollback/disable controls, and incident ownership. Evidence must identify exact commit, environment, configuration, scope, and date. Outcomes: PASS (evidence and no blocking findings); PASS WITH ACCEPTED RISK (only authorized, scoped, unexpired risks); BLOCKED (missing evidence or blocking finding); NOT APPLICABLE (genuine irrelevance with rationale). Missing evidence is never PASS.

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
