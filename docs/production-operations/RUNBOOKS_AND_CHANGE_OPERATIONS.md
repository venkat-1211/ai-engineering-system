# Runbooks and Change Operations

## Runbook quality
A runbook states purpose, scope, prerequisites, required access, safe steps, expected results, verification, rollback, escalation and last-reviewed date. Avoid embedding credentials or sensitive operational details.

## Change control
Record purpose, scope, risk, affected services, dependencies, test evidence, approval, deployment window where relevant, monitoring plan and rollback criteria. Approval must come from an authorized human.

## Production execution
AI agents may prepare commands and explain risks. They must not execute production changes unless explicitly authorized within the applicable tool and organizational controls. Destructive or irreversible operations require explicit confirmation.

## Rollback
Define rollback triggers and steps before a risky change. Verify rollback feasibility and data compatibility. Some database or data migrations cannot be safely reversed; document forward-recovery alternatives.

## Review
After the change, record actual outcome, deviations, incidents and follow-up work.
