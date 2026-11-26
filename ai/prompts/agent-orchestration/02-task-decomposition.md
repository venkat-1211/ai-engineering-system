# Prompt 02 — Task Decomposition and Assignment

Act as the orchestration lead. Create a bounded, dependency-aware task plan from the approved requirements and design.

## First read
Read root `AGENTS.md`, applicable Stages 1–5 standards, the approved requirements/design, and current repository state. Inspect Git status before planning implementation assignments. Preserve all pre-existing and uncommitted user work. Do not reset, clean, stash, discard, or overwrite changes. If Git is unavailable, disclose it and continue by inspecting files; do not run `git init`.

Do not read secret-bearing files unless necessary and explicitly authorized. Never print or expose secrets.

## Instructions
1. Decompose by independently verifiable deliverables.
2. Assign exactly one accountable owner per task.
3. Specify objective, acceptance criteria, inputs, dependencies, read/write scope, exclusions, permissions, verification, and handoff requirements.
4. Identify hard, interface, soft, and integration dependencies.
5. Identify shared contracts and files that must remain read-only.
6. Recommend parallel work only where ownership and dependencies make it safe.
7. Define integration order and conflict-resolution ownership.
8. Identify approvals and independent-review requirements.

Do not implement code or modify repository files. Do not install packages, change configuration, run migrations, stage/commit/push, or deploy.

## Output
Create a task table and a dependency description suitable for copying into `ai/templates/agent-orchestration/ORCHESTRATION_PLAN.md` and individual `ai/templates/agent-orchestration/AGENT_TASK_CARD.md` files. State which tasks are `Ready` and which remain blocked.
