# Task Decomposition and Dependencies

## Decomposition method

1. Start from the approved user outcome and acceptance criteria.
2. Identify deliverables and system boundaries.
3. Inspect the repository and actual technology versions before assigning implementation work.
4. Split work by independently verifiable outcome, not merely by file count.
5. Identify prerequisites, shared contracts, data ownership, and integration points.
6. Assign one accountable owner per task.
7. Define scope, allowed files, prohibited actions, tests, and handoff evidence.
8. Confirm the task graph has no missing dependency or circular dependency.

## A good task is

- small enough for one owner to complete and explain;
- bounded by explicit inputs and outputs;
- testable against acceptance criteria;
- clear about files/components it may change;
- explicit about dependencies and blockers;
- sized to fit the available agent context.

## Dependency types

- **Hard dependency:** downstream task cannot safely start until upstream output is accepted.
- **Interface dependency:** tasks may proceed after a shared contract is agreed.
- **Soft dependency:** work can proceed with a documented assumption, subject to confirmation.
- **Integration dependency:** separate outputs must be combined and tested together.

Never disguise a hard dependency as parallel work.

## Task readiness

A task is `Ready` only when its owner, scope, inputs, acceptance criteria, dependencies, and permissions are clear. Otherwise it remains `Not started` or `Blocked`.

## Change control

If an agent discovers additional scope, it must stop the expansion, report the reason and impact, and request an updated assignment or human decision. Do not silently absorb unrelated cleanup.
