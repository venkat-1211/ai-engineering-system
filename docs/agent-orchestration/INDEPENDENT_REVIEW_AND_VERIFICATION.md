# Independent Review and Verification

## Review objective

Determine whether the delivered change satisfies the approved requirements and repository standards. Review evidence, not confidence or persuasive wording.

## Independence requirements

- The reviewer should not rely solely on the implementer's summary.
- Provide the reviewer with acceptance criteria, relevant standards, actual diffs, and test evidence.
- For high-risk changes, separate implementation and approval roles where feasible.
- The reviewer must disclose any shared context or limitation that weakens independence.

## Review dimensions

- requirements and acceptance-criteria coverage;
- correctness, edge cases, and regression risk;
- security, privacy, authorization, and input validation;
- data integrity and migration safety;
- performance and reliability;
- maintainability and architecture consistency;
- accessibility and user experience where relevant;
- tests and quality-gate evidence;
- documentation, configuration, and rollback implications.

## Finding format

Each finding should include severity, affected path/area, evidence, impact, reproduction or reasoning, and recommended action. Separate confirmed defects from questions and suggestions.

## Verification statuses

Use the repository's five verification statuses consistently:
- `Passed` — actually executed and passed, with evidence.
- `Failed` — executed and failed, with evidence.
- `Not run` — not executed.
- `Blocked` — could not execute, with reason.
- `Requires human approval` — action or decision awaits explicit approval.

An agent's self-report is not independent verification. A review with no findings does not prove that untested behavior works.
