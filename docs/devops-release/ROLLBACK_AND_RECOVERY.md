# Rollback & Recovery

Every release must identify:
- Rollback/forward-recovery decision owner.
- Known-good artifact and its digest.
- Trigger thresholds and decision deadline.
- Procedure, access requirements, expected duration, and verification steps.
- Database/schema/data compatibility constraints.
- Backup/restore dependencies and evidence.
- Customer and internal communications responsibilities.

Test recovery in a safe environment at a frequency proportionate to risk. Prefer reversible deployment patterns. Do not promise rollback when irreversible data changes or external side effects make it impossible; define a forward-fix or compensating action instead.

After recovery, preserve logs and timelines, verify service and data integrity, and complete incident/postmortem actions under Stage 7.
