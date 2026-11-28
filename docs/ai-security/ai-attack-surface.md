# Ai Attack Surface

Inventory user prompts, uploads, conversation history, retrieved documents, websites, emails, connected apps, system/developer prompts, memory, model/provider APIs, plugins, tool schemas, generated text/code/SQL/HTML/URLs, files, logs, traces, caches, vector stores, backups, analytics, CI/CD, package registries, model artifacts, and deployment secrets. For each record owner, data class, trust level, authentication, authorization, validation, limits, logging, retention, failure behavior, and tests. Assume untrusted inputs can influence model outputs. Enforce controls at deterministic boundaries.

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
