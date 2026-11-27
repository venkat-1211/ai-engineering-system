# Test Design and Meaningful Assertions

## Test structure
Use clear Arrange/Act/Assert or Given/When/Then structure. Each test should have a focused purpose and explain non-obvious setup.

## Assertions
Assert externally meaningful outcomes: response, persisted state, emitted event, permission decision, side effect, or user-visible behavior. Avoid assertions that merely repeat the implementation or always pass.

## Coverage of behavior
Consider normal paths, invalid inputs, boundaries, missing data, unauthorized access, dependency failures, retries, timeouts, race conditions, duplicate requests, and recovery paths as appropriate.

## Independence and determinism
Tests should not depend on order, shared mutable state, wall-clock timing, external network availability, or production data unless explicitly designed and controlled. Use stable clocks, isolated fixtures, controlled fakes, and cleanup.

## Maintainability
Prefer readable test names and helpers that reduce duplication without hiding intent. Avoid giant fixtures, excessive mocking, and brittle selectors. Review whether a test would fail if the target behavior regressed.
