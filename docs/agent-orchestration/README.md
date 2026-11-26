# Agent Orchestration Standards

## When to orchestrate

Use multiple agents when work has meaningful separable streams, specialist review needs, or enough complexity to justify coordination overhead. Prefer one agent for a small bug, simple copy change, isolated refactor, or straightforward question.

Before starting, establish:
- the user outcome and acceptance criteria;
- repository and environment boundaries;
- applicable Stages 1–4 standards;
- task owners and permitted write scopes;
- dependencies and integration order;
- review and human-approval gates.

## Operating sequence

1. **Intake:** clarify the outcome, constraints, risk, and definition of done.
2. **Plan:** choose the orchestration pattern and create an orchestration plan.
3. **Decompose:** create bounded tasks with one accountable owner each.
4. **Assign:** provide each agent only the context and permissions needed.
5. **Execute:** track progress, dependencies, decisions, and blockers.
6. **Integrate:** reconcile outputs and resolve conflicts deliberately.
7. **Verify:** run appropriate tests and independent reviews; report actual evidence.
8. **Close:** summarize delivered work, limitations, and follow-up actions.

## Source of truth

The orchestrator maintains the current plan, task status, dependency graph, decision log, and final consolidated report. If a tool cannot share state between agents, use explicit written handoffs; do not assume agents can see each other's conversations or files.

## Required statuses

Keep task-progress statuses and verification statuses strictly separate; do not mix them in the same status list.

### Task-progress statuses
Describe workflow progress for a task:
- `Not started`
- `Ready`
- `In progress`
- `Blocked`
- `Review required`
- `Cancelled`

### Verification statuses
Describe the outcome or state of a verification check:
- `Passed`
- `Failed`
- `Not run`
- `Blocked`
- `Requires human approval`

**Status rules:**
- `Passed` is permitted only when the check was actually executed and passed with recorded evidence. A task is not verified merely because an agent says it is complete; the owner must provide evidence and required reviewers must accept it.
- `Blocked` can apply to either a task or a verification check, but its meaning must be clear from the category (a task unable to proceed vs. a check that could not be executed due to a stated blocker).

## Required outputs

For medium/high-complexity work, create an orchestration plan and task cards. Use handoff reports at agent boundaries and a decision log for material choices. Scale documentation to risk; do not create process overhead for trivial work.

## Related standards

- `docs/agent-orchestration/MULTI_AGENT_OPERATING_MODEL.md`
- `docs/agent-orchestration/ROLE_CATALOG.md`
- `docs/agent-orchestration/ORCHESTRATION_PATTERNS.md`
- `docs/agent-orchestration/TASK_DECOMPOSITION_AND_DEPENDENCIES.md`
- `docs/agent-orchestration/HANDOFF_AND_CONTEXT_PROTOCOL.md`
- `docs/agent-orchestration/PARALLEL_EXECUTION_AND_CONFLICT_CONTROL.md`
- `docs/agent-orchestration/INDEPENDENT_REVIEW_AND_VERIFICATION.md`
- `docs/agent-orchestration/HUMAN_APPROVAL_AND_ESCALATION.md`
- `docs/agent-orchestration/CONTEXT_AND_TOKEN_EFFICIENCY.md`
- `docs/agent-orchestration/FAILURE_RECOVERY_AND_STOP_CONDITIONS.md`
