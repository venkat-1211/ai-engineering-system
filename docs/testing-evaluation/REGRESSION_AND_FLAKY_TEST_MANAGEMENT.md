# Regression and Flaky Test Management

## Regression strategy
Maintain tests for important user journeys, historical defects, security boundaries, and critical contracts. Link regression cases to the defect or requirement they protect.

## Flaky tests
A flaky test produces inconsistent outcomes without a relevant code change. Record frequency, environment, failure signatures, and suspected cause. Do not normalize repeated retries as success.

## Quarantine
Quarantine only through an approved, visible process with owner, reason, issue reference, impact, compensating coverage, expiry/review date, and explicit CI behavior. A quarantined test must not silently count as passed.

## Repair priority
Prioritize flakes by criticality, frequency, pipeline impact, and risk of hidden regressions. Fix nondeterminism rather than increasing retries indefinitely.

## Regression after fixes
Add or update a test that would have detected the defect. Verify the fix and relevant neighboring behavior.
