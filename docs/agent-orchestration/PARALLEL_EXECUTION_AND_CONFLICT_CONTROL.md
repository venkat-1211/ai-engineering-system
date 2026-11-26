# Parallel Execution and Conflict Control

## Preconditions for parallel work

Parallel execution is permitted only when:
- tasks have clear, separate outcomes;
- dependencies are satisfied or explicitly soft;
- shared interfaces are agreed;
- write scopes do not overlap, or a safe integration method is confirmed;
- the tool supports the required isolation and state visibility;
- each agent has bounded permissions.

If any precondition is unknown, use sequential execution.

## File ownership

For each parallel task, list:
- files/directories it may modify;
- files it may read;
- files owned by another task;
- shared files that are read-only;
- integration owner.

No two agents should write the same file concurrently unless the platform provides a verified conflict-safe mechanism and the orchestrator explicitly coordinates it.

## Integration

1. Freeze or record the task outputs.
2. Inspect actual diffs and changed-file lists.
3. Detect overlapping edits and incompatible assumptions.
4. Resolve conflicts with the accountable owner.
5. Integrate in dependency order.
6. Run relevant unit, integration, security, and regression checks.
7. Obtain independent review where required.

## Conflict response

On a conflict, stop affected writes. Preserve both versions and user work. Do not use reset, clean, force checkout, or overwrite operations to resolve it. Ask the orchestrator/human to decide when intent is ambiguous.

## Tool limitations

Do not claim parallel execution if tasks were actually performed sequentially. Do not assume an agent can see another agent's branch, files, messages, or test results without verifying the platform behavior.
