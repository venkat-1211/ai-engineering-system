# AI Engineering System — Stage 2

Stage 2 adds tool-specific instruction adapters on top of Stage 1.

## Installation
1. Keep the Stage 1 files in place.
2. Merge these files into the project root. Review existing files before overwriting.
3. If AGENTS.md, CLAUDE.md, .github/, .claude/, .codex/ or .agents/ already exists, merge carefully.
4. Review `.codex/config.toml` and understand its sandbox/approval behavior before trusting the project.
5. `.claude/settings.example.json` is an example only; it is not active until reviewed and copied to `settings.json`.
6. Restart or reload agent sessions where required.
7. Run `ai/prompts/verify-agent-instructions.md` separately with each coding tool.

## Windows user-level locations
- Codex: `%USERPROFILE%\\.codex\\config.toml`
- Claude Code: `%USERPROFILE%\\.claude\\settings.json`
- Antigravity global rules: under `%USERPROFILE%\\.gemini\\` (surface-dependent).

Instruction files are not security boundaries. Use runtime permissions, OS/container sandboxing, CI checks, application authorization and human approval. Verify active instructions in each exact tool surface.
