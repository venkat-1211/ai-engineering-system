# Stage 7 — Production Operations, Observability & Reliability Engineering

## Purpose
Stage 7 defines repeatable operational practices for software after deployment: observability, service reliability, incident response, recovery, capacity, operational security and continual operational improvement.

Stage 7 extends Stages 1–6. It does not replace their engineering, technology, lifecycle, orchestration or governance rules.

## Integration
1. Extract this package into the repository root, preserving paths.
2. Review every file and integrate the Stage 7 references into the existing root `AGENTS.md`.
3. Keep `AGENTS.md` as the active repository-wide source of truth. Do not paste the entire Stage 7 documentation into it.
4. Preserve all existing stages and instructions. Add concise links and operational requirements in the relevant existing sections; do not renumber or rewrite unrelated sections.
5. Follow the separate repository integration instructions to update `AGENTS.md`, and complete a separate read-only Stage 7 pre-commit audit before committing. (The six prompts in `ai/prompts/production-operations/` are for assessing a project's production operations; they are not repository integration or Stage 7 package audit prompts.)
6. Do not stage, commit or push until the user explicitly approves and the final read-only audit passes.

## Package contents
- `docs/production-operations/`: operational standards and procedures.
- `ai/templates/production-operations/`: reusable operational records.
- `ai/checklists/production-operations/`: operational readiness and review gates.
- `ai/prompts/production-operations/`: controlled AI workflows.

## Operating principles
- Production actions require explicit authorization and an identified human owner.
- Never claim monitoring, backup, restore, alerting, failover or recovery works without execution evidence.
- Do not expose secrets, credentials, tokens, personal data or sensitive operational details in reports.
- Define service objectives only with stakeholders and measurable evidence; do not invent SLOs or availability targets.
- Prefer reversible, tested operational changes and documented rollback plans.
- Apply controls proportionally to system criticality, risk, architecture and team capacity.
- A documented runbook is not proof that the procedure has been tested.

## Scope boundaries
Stage 7 is a standards and workflow package, not an implementation of monitoring infrastructure, CI/CD, backup services, incident tooling or cloud resources. Those are project-specific decisions.
