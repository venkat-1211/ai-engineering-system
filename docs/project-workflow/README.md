# Project Workflow Standards

This directory defines the lifecycle used to plan, build, verify, release, and maintain software.

## Documents

1. `PROJECT_LIFECYCLE.md` — end-to-end workflow and approval gates.
2. `REQUIREMENTS_ENGINEERING.md` — problem framing, scope, requirements, assumptions, and acceptance criteria.
3. `SOLUTION_DESIGN.md` — repository discovery, architecture, technology decisions, and design review.
4. `DATA_AND_API_DESIGN.md` — database, API, integration, and compatibility design.
5. `IMPLEMENTATION_PLANNING.md` — phases, tasks, dependencies, sequencing, and definition of done.
6. `AI_AGENT_ORCHESTRATION.md` — role separation, context sharing, permissions, and independent review.
7. `QUALITY_AND_RELEASE.md` — verification, release readiness, rollback, and operations.
8. `CHANGE_AND_MAINTENANCE.md` — change control, incidents, technical debt, and ongoing ownership.

## Relationship to Stage 1 workflow

- `docs/AI_DEVELOPMENT_WORKFLOW.md` is the concise task-level AI development workflow.
- `docs/project-workflow/PROJECT_LIFECYCLE.md` expands that workflow into a complete end-to-end project lifecycle.
- Stage 4 complements Stage 1 rather than replacing it.
- Use the full Stage 4 lifecycle for medium/high-complexity projects and significant changes; for small tasks, use the concise workflow and only the relevant Stage 4 gates.

## How to use

Start with the lifecycle document. Select only the standards relevant to the project and task. Use templates and checklists as needed. The workflow is risk-based: a one-line copy change does not need a full architecture pack, while a payment, authentication, data migration, or production infrastructure change requires deeper review.
