# AI Security Engineering Standards

AI security is a lifecycle responsibility across design, implementation, testing, deployment, and operations. Identify assets, actors, trust boundaries, and abuse cases; implement preventive/detective/recovery controls; test; record evidence and residual risks; monitor and improve. Apply these standards to chat, RAG, agents, tool calling, code generation/execution, model APIs, and AI-assisted workflows. Tailor controls to actual architecture and document non-applicability.

## Standards
- `docs/ai-security/threat-modeling.md` — threat modeling methodology, abuse cases, and deliverables.
- `docs/ai-security/ai-attack-surface.md` — AI attack-surface inventory and deterministic boundaries.
- `docs/ai-security/prompt-injection.md` — direct/indirect prompt injection defenses and testing.
- `docs/ai-security/agent-tool-security.md` — deny-by-default tool allowlists, validation, and approvals.
- `docs/ai-security/authentication-authorization.md` — identity separation, least privilege, and fail-closed authorization.
- `docs/ai-security/data-protection.md` — classification, tenant isolation, retrieval authorization, and retention.
- `docs/ai-security/secrets-management.md` — credential storage, redaction, rotation, and exposure response.
- `docs/ai-security/sandboxing-isolation.md` — OS/container/VM/network isolation and resource limits.
- `docs/ai-security/supply-chain-security.md` — dependency, model, provider, tool, and prompt supply-chain review.
- `docs/ai-security/adversarial-testing.md` — threat-derived adversarial security testing and evidence.
- `docs/ai-security/security-findings.md` — finding lifecycle, severity rubric, and accepted-risk governance.
- `docs/ai-security/incident-response.md` — AI security incident triggers, containment, and evidence preservation.
- `docs/ai-security/security-release-gates.md` — evidence-based security release gate criteria and outcomes.

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
