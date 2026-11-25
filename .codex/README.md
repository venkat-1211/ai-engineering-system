# Codex project configuration

- `AGENTS.md` is the primary project instruction file.
- `.codex/config.toml` is an optional project-scoped runtime configuration example.
- Project config is loaded only for a trusted project.
- The example uses on-request approvals, workspace-write sandboxing and disabled sandbox network access.
- These controls are not a substitute for OS/container isolation, least-privilege credentials, Git review or human approval.
- Check the current Codex configuration reference and behavior for your OS/CLI version.
- Do not use `danger-full-access` or disable approvals as a convenience default.
- Keep personal/global settings in the user's Codex home directory, not in a shared repository.
