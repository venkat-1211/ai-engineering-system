# Stage 4 — Project Engineering Workflow

Stage 4 adds a repeatable, approval-gated workflow for taking software work from an initial idea or change request through requirements, architecture, implementation, verification, release, and maintenance.

## Purpose

Use this workflow for new applications, features, integrations, refactors, bug fixes, migrations, and operational changes. Scale the depth of each artifact to the risk and size of the task; do not create heavyweight paperwork for a trivial change.

## Installation

1. Extract this Stage 4 archive into a temporary folder.
2. Review the files before merging them into your existing AI Engineering System repository.
3. Copy the `docs/project-workflow/`, `ai/templates/project-workflow/`, `ai/checklists/project-workflow/`, and `ai/prompts/project-workflow/` directories into the matching locations in your repository.
4. Do not replace your existing root `AGENTS.md`. Merge the short guidance from `AGENTS_STAGE_4_ADDENDUM.md` into the appropriate existing sections.
5. Review the workflow against your actual team, risk level, and delivery process.
6. Commit the merged files only after reviewing the diff.

## Recommended workflow

| Gate | Work | Required decision |
|---|---|---|
| 0. Intake | Understand request, users, problem, constraints | Is the request understood well enough to investigate? |
| 1. Requirements | Scope, functional/non-functional requirements, acceptance criteria | Are requirements testable and agreed? |
| 2. Solution design | Stack discovery, architecture, data/API design, risks | Is the proposed solution safe and feasible? |
| 3. Delivery plan | Phases, tasks, dependencies, test strategy | Is the plan implementable and appropriately sequenced? |
| 4. Implementation | Small, reviewable changes with tests | Does each increment meet its acceptance criteria? |
| 5. Verification | QA, security, regression, performance as applicable | Is there evidence that the change works? |
| 6. Release | Deployment, migration, rollback, monitoring | Is release approved and recoverable? |
| 7. Operations | Observe, support, learn, maintain | Is the system healthy and ownership clear? |

A gate is not a claim that every document must exist. It is a decision point. For low-risk work, concise notes may be enough. For high-risk work, require explicit review and evidence.

## Files

- `docs/project-workflow/` — workflow and decision standards.
- `ai/templates/project-workflow/` — reusable project artifacts.
- `ai/checklists/project-workflow/` — gate and quality checklists.
- `ai/prompts/project-workflow/` — reusable agent prompts.
- `AGENTS_STAGE_4_ADDENDUM.md` — small, safe guidance to merge into the existing root instructions.

## Operating rules

- No implementation before the request, scope, and acceptance criteria are sufficiently clear.
- Do not invent requirements. Record assumptions and ask focused questions when an ambiguity changes scope, security, data, or behavior.
- Discover the actual repository, stack, versions, architecture, conventions, and existing behavior before proposing changes.
- Prefer the smallest safe solution that meets the accepted requirements.
- Separate confirmed facts, assumptions, decisions, and open questions.
- Require human approval for production-impacting, destructive, costly, externally visible, or security-sensitive actions.
- Tests must be run and reported honestly. “Not run” is not “passed”.
- A release must have a rollback or recovery approach appropriate to its risk.
- Keep documentation proportionate and update it when implementation changes the documented truth.

## Relationship to previous stages

Stage 4 builds on the shared engineering rules in root `AGENTS.md`, tool adapters from Stage 2, and technology standards from Stage 3. It does not replace them. If there is a conflict, follow the instruction precedence defined in the existing root `AGENTS.md` and resolve ambiguity before acting.
