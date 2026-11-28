# Prompt 01 — DevOps Discovery & Baseline

Act as a read-only DevOps assessment engineer. Inspect the repository and supplied project context without changing files, running deployments, accessing production secrets, or modifying infrastructure.

Report:
1. Repository, branch model, protections (only where observable), owners, and release tags.
2. Build/test/lint/security workflows and exact file paths.
3. Runners, external actions, images, registries, and dependency pinning.
4. Environments, deployment paths, identities, and configuration sources (never reveal secret values).
5. Artifact storage, provenance, promotion, and retention.
6. IaC, state handling, drift, and approval controls.
7. Release, migration, rollback, and post-deployment verification practices.
8. Gaps mapped to Stage 11 standards with severity and evidence.

Distinguish verified facts from assumptions and unknowns. Do not claim controls exist unless directly evidenced. End with prioritized recommendations. No edits, installs, commits, pushes, or production actions.
