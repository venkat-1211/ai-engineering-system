# Failure Recovery and Stop Conditions

## Common failure modes

- duplicate or overlapping implementation;
- conflicting architecture decisions;
- stale repository context;
- missing dependencies or unavailable tools;
- agent timeout or incomplete output;
- unverified claims about tests or commands;
- scope drift;
- accidental edits outside assigned ownership;
- integration failures after parallel work.

## Recovery procedure

1. Stop the affected task or writes.
2. Preserve current files and user changes.
3. Record what was attempted and what actually happened.
4. Identify the last known-good state using read-only inspection.
5. Separate confirmed facts from assumptions.
6. Notify the orchestrator and identify the impact.
7. Propose the smallest safe recovery options.
8. Obtain human approval if recovery is destructive, irreversible, external, costly, or outside scope.
9. Re-run affected verification after approved recovery.
10. Update task status, handoff, and decision log.

## Never

- hide or overwrite another agent's work;
- claim success after a timeout without checking state;
- repeat a failed destructive operation automatically;
- use `git reset --hard`, `git clean`, force checkout, or similar destructive commands to resolve orchestration conflicts;
- suppress failing tests or lower quality gates merely to close a task.

## Status and escalation

Use `Blocked` when progress cannot safely continue. Use `Failed` for an executed check that failed. Use `Not run` when it was not executed. Escalate unresolved ambiguity or authorization issues to the human owner.
