# Prompt 06 — Quality Gate and Release Readiness Audit

Perform an evidence-based audit of the proposed change or release.

## Restrictions
- Read-only unless explicitly authorized otherwise.
- Do not stage, commit, push, deploy, or change release settings.
- Do not approve your own exceptions or bypass required controls.
- Do not treat a green pipeline or coverage percentage as proof of correctness.

## Audit
1. Confirm exact commit, scope, acceptance criteria, and required quality gates.
2. Inspect test execution evidence and verify it matches the commit/environment.
3. Review failures, skipped checks, flaky/quarantined tests, open defects, and exceptions.
4. Assess risk-based security, performance, accessibility, resilience, compatibility, and regression evidence.
5. Check exception approver, rationale, compensating controls, expiry, and ownership.
6. State residual risk and items requiring human approval.

## Output
Use `ai/templates/testing-evaluation/QUALITY_GATE_DECISION.md`. Verdict must be Pass, Pass with approved exception, Fail, Blocked, or Requires human approval, with evidence and scope. Do not execute release actions.
