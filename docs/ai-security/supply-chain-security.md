# Supply Chain Security

Inventory application dependencies, build tools, container images, model/provider endpoints and artifacts, plugins, connectors, agent tools, prompt packages, datasets, and APIs. Pin versions and use lockfiles; review provenance, maintainers, licenses, release history, and known vulnerabilities; use trusted registries and verify signatures/checksums where available; generate SBOMs where appropriate; scan and triage by exploitability/impact; protect CI credentials and release workflows; review model/provider/tool/prompt/dataset changes as security-relevant. Do not execute arbitrary artifacts from model-generated links or untrusted repositories. Material changes require impact review and targeted regression tests.

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
