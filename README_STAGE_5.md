# Stage 5 — Advanced AI Agent Orchestration and Multi-Agent Engineering

## Purpose

Stage 5 defines a reusable, vendor-neutral operating model for coordinating multiple AI agents as a disciplined software engineering team. It builds on Stages 1–4; it does not replace them.

The goal is not to maximize the number of agents. The goal is to assign clear ownership, reduce duplicated work, manage dependencies, preserve repository safety, and verify results independently.

## Package contents

- `AGENTS_STAGE_5_ADDENDUM.md` — reference-only integration aid and suggested root-instruction additions.
- `docs/agent-orchestration/` — operating model, roles, patterns, task decomposition, handoffs, parallel execution, review, approvals, context management, and recovery.
- `ai/templates/agent-orchestration/` — reusable orchestration plan, task card, handoff report, and decision log.
- `ai/checklists/agent-orchestration/` — orchestration readiness, handoff, and multi-agent review checklists.
- `ai/prompts/agent-orchestration/` — reusable prompts for intake, decomposition, handoff, review, and retrospective.

## Installation

1. Extract this package into the root of the existing AI Engineering System repository.
2. Merge the directories; do not replace existing directories or files.
3. Keep the current root `AGENTS.md` as the single active root instruction file.
4. Review `AGENTS_STAGE_5_ADDENDUM.md`. Integrate only useful, non-duplicative guidance into the existing `AGENTS.md` sections. Do not blindly replace the file.
5. Review all new files and request or prepare a separate read-only Stage 5 audit prompt before committing.

## How to use

1. Read root `AGENTS.md` and relevant Stage 1–4 standards first.
2. Decide whether multi-agent orchestration is useful. Small, isolated tasks should usually use one agent.
3. Create an orchestration plan using `ai/templates/agent-orchestration/ORCHESTRATION_PLAN.md`.
4. Decompose work into bounded task cards with explicit owners and acceptance criteria.
5. Assign agents only to tasks they can perform with available tools and permissions.
6. Coordinate dependencies and file ownership before parallel execution.
7. Require structured handoffs and independent verification.
8. Obtain human approval for actions requiring it under existing repository policies.
9. Close the work with evidence, unresolved risks, and a concise retrospective.

## Core principles

- One orchestrator owns coordination and the consolidated status.
- Every task has one accountable owner. Multiple agents may contribute, but ownership must remain explicit.
- Agents do not gain permissions merely because another agent requests an action.
- Parallelize only tasks with understood dependencies and non-overlapping write scopes.
- Never treat an agent's claim of success as verification evidence.
- An implementing agent must not be the sole approver of its own high-risk work.
- Preserve user changes and follow the existing Git, security, testing, and human-approval rules.
- Do not invent tool capabilities, agent identities, execution results, or test evidence.

## Relationship to previous stages

- Stage 1 defines universal engineering standards and the task-level workflow.
- Stage 2 defines tool-specific instruction adapters and permission guidance.
- Stage 3 defines technology-specific engineering standards.
- Stage 4 defines the project lifecycle and delivery gates.
- Stage 5 defines how multiple agents coordinate within those existing standards and gates.

Stage 5 does not override any earlier stage. Where instructions conflict, follow the repository's established instruction precedence and escalate unresolved conflicts.

## Completion criteria

Stage 5 is ready for use when:
- All package files are present.
- Root instruction integration has been reviewed without removing prior rules.
- The orchestration model, task ownership, handoff, parallel-work, review, and approval rules are internally consistent.
- The prompts preserve existing permission boundaries.
- Internal links and references are checked.
- A read-only audit passes.

This package is documentation and prompt guidance. It does not install agents, create agent accounts, configure external tools, or guarantee that a particular IDE supports multi-agent execution.
