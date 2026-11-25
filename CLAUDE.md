# Claude Code project guidance

@AGENTS.md
@docs/AI_ENGINEERING_STANDARD.md
@docs/AI_DEVELOPMENT_WORKFLOW.md
@docs/AI_AGENT_INSTRUCTION_MAP.md

Keep shared engineering policy in the referenced files; keep this adapter concise.

- Use Plan Mode or present a plan before cross-cutting, destructive, security-sensitive or materially ambiguous work.
- Use subagents for bounded, independent read-only investigations or reviews when useful.
- Review subagent findings before acting. Avoid concurrent edits to the same files.
- Use hooks and permission controls for deterministic safeguards; natural-language rules are not enforcement.
- Do not automatically approve broad shell, filesystem, network, browser, MCP or production permissions.
- Inspect the final diff and report actual verification results.
