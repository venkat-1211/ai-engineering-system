# Release Gate Checklist

This gate provides the Stage 4 project lifecycle release decision. Use it alongside `ai/checklists/production-readiness.md`, which supplies the applicable Stage 3 technology and production-readiness checks.

- [ ] Release scope and owner are confirmed.
- [ ] Acceptance criteria are satisfied.
- [ ] Applicable tests were actually executed and passed, with execution evidence (command/tool and result) recorded for every check marked `Passed`.
- [ ] Each check is reported using one exact status: `Passed` (actually executed and succeeded), `Failed` (executed and failed), `Not run` (not executed), `Blocked` (could not execute because of a blocker), or `Requires human approval` (requires an authorized human decision).
- [ ] Legitimately inapplicable checks, exceptions, `Failed`/`Not run`/`Blocked` items, and unresolved release blockers are transparently disclosed.
- [ ] Security and dependency findings are reviewed.
- [ ] Configuration and secret handling are reviewed.
- [ ] Database/data migration and integrity plan are reviewed.
- [ ] Backup and restore/recovery approach is available.
- [ ] Rollback or forward-fix plan is documented.
- [ ] Monitoring, alerts, logs, and support ownership are ready.
- [ ] Required human approvals are obtained.
- [ ] Post-deployment verification steps are defined.

Gate result: Ready / Not ready / Blocked / Requires human approval
Evidence / notes:
