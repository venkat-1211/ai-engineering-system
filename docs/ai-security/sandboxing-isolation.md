# Sandboxing Isolation

Use isolation for untrusted code, generated scripts, uploaded files, browser automation, converters, plugins, and tools affecting host resources. Separate execution from production control planes and sensitive stores; use non-root identities and read-only filesystems where feasible; narrowly mount paths; restrict network egress and block metadata/internal networks unless explicitly required; set CPU/memory/process/file/time/concurrency limits; use disposable workspaces; validate files; keep credentials outside the sandbox; record execution metadata and terminate runaway work. Verify actual OS/container/VM/network controls. A prompt is not a sandbox.

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
