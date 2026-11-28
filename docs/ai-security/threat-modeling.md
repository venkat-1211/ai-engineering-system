# Threat Modeling

## Method
1. Define purpose, scope, deployment, data classes, identities, providers, tools, autonomy, and business impact.
2. Diagram components, data flows, stores, external services, and trust boundaries.
3. Identify assets (credentials, personal/confidential data, tenant data, prompts, model configuration, tools, audit evidence) and actors (users, attackers, compromised accounts, malicious content authors, insiders, dependencies, providers).
4. Enumerate abuse cases using STRIDE or an approved method plus AI-specific cases.
5. Rate likelihood/impact using the organization's approved rubric; do not invent scores.
6. Map preventive, detective, and recovery controls to risks; assign owners and evidence.
7. Revisit after model, prompt, tool, data, provider, architecture, or permission changes.

Minimum scenarios: direct/indirect prompt injection, retrieval poisoning, sensitive-data disclosure, cross-tenant leakage, unauthorized tool execution, privilege escalation, unsafe generated code, provider compromise, resource exhaustion, and downstream output injection.

Deliverables: current data-flow/trust-boundary diagram, threat register, control mapping, test plan, residual-risk decisions, owner, and review date. Use `ai/templates/ai-security/threat-model.md`.

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
