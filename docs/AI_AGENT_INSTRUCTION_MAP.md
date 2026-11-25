# AI Agent Instruction Map

The selected harness determines which files are loaded; the model does not automatically read every file.

| Tool | Main project instruction | Additional configuration | How to verify |
|---|---|---|---|
| Codex | `AGENTS.md` | Optional `.codex/config.toml` | Ask Codex to summarize active instructions; inspect trust/config |
| GitHub Copilot | `.github/copilot-instructions.md`; `AGENTS.md` where supported | `.github/instructions/*.instructions.md` | Check support for exact IDE/CLI/cloud/review surface |
| Claude Code | `CLAUDE.md` importing shared files | `.claude/rules/`, optional `.claude/settings.json` | `/status`; inspect loaded settings |
| Antigravity | `AGENTS.md`, `.agents/rules/*.md` | Workspace/global Customizations | Inspect active rules in Customizations |

## Source-of-truth policy
- `AGENTS.md` and Stage 1 standards contain shared engineering policy.
- Tool-specific files adapt discovery and tool behavior only.
- Avoid copying full standards into every adapter.
- Resolve conflicts instead of allowing duplicate contradictory rules.
- Do not assume all clients and versions support identical instruction formats.

## Layering
1. Global user preferences.
2. Repository engineering and project standards.
3. Directory/path-specific rules.
4. Current task prompt and acceptance criteria.
5. Runtime permissions and sandbox controls.

## Safe defaults
Use read/plan-first behavior for unfamiliar workspaces, limit filesystem scope to the repository, keep network disabled unless approved and necessary, retain approval prompts for elevated/destructive actions, and never use unrestricted access as a routine default.
