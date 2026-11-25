# AI Agent Permissions and Safe Configuration Guide

Instruction files influence behavior; runtime permissions and OS isolation enforce boundaries. Use both.

## General
- Grant only tools and directories needed.
- Prefer read-only inspection before edits.
- Keep network disabled unless a specific approved task requires it.
- Require approval for destructive commands, production access, external publishing, credential access and deployments.
- Do not expose production credentials to general coding agents.
- Use a disposable branch/worktree/container for risky changes.

## Claude Code
- Use `CLAUDE.md` and `.claude/rules/` for guidance.
- Use `.claude/settings.json` only for intentional shared settings; keep personal overrides local.
- `settings.example.json` is not active. Review denied paths and syntax before copying it.
- Verify loaded settings with `/status`; use `claude doctor` for configuration errors.
- Avoid broad Bash allow rules.

## Codex
- Use `AGENTS.md` for project instructions.
- `.codex/config.toml` is a project-scoped example and is loaded only after project trust.
- `on-request` preserves approval prompts; `workspace-write` restricts writes according to Codex sandbox behavior; network is disabled in the example.
- Do not use `danger-full-access` as a default. Check current official guidance and OS support.

## GitHub Copilot
Instruction support differs by IDE, CLI, cloud agent and code-review feature. Verify the support matrix for the exact surface.

## Antigravity
Workspace rules support `AGENTS.md` and `.agents/rules/*.md`. Rules in `.agents/rules/` require valid YAML frontmatter and a supported trigger. Verify active rules in Customizations.

## Before expanding permissions
Ask what task needs the permission, which tool/path needs it, whether read-only or disposable execution is possible, what sensitive systems/data are exposed, and how access will be revoked.
