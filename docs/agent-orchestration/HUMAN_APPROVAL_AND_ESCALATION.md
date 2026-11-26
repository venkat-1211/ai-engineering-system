# Human Approval and Escalation

## Approval principle

Agents may analyze and recommend actions, but may not bypass repository policy or user approval requirements. Stage 1–4 safety and approval rules remain authoritative.

## Always escalate when

- requirements are ambiguous in a way that changes scope or user-visible behavior;
- a task requires destructive or irreversible action;
- production state, live data, customer communication, or external services may be affected;
- an action incurs cost, sends messages, creates accounts, or exposes information externally;
- credentials, secrets, personal data, or access permissions are involved;
- a dependency, license, architecture, or security decision has material impact;
- agents disagree on a material design or safety decision;
- user-owned changes may be overwritten;
- a test failure cannot be safely explained or resolved within scope.

## Approval record

Record the action, reason, expected impact, risk, alternatives, rollback/recovery approach, approver, and approval evidence. Approval for analysis is not approval for execution.

## Stop conditions

Stop the affected task when authorization is missing, scope is unclear, evidence is unreliable, a secret is exposed, destructive impact is possible, or the environment differs materially from the approved plan.

Do not continue through a blocker by inventing assumptions or weakening controls.
