# Database & Data Migration Releases

## Before release
- Identify schema, data, index, constraint, and application compatibility impacts.
- Estimate duration, locking, storage, replication, and user-visible effects.
- Test migration against representative non-production data volumes where feasible.
- Confirm backup freshness and restore evidence appropriate to risk.
- Define preconditions, progress monitoring, abort conditions, and recovery owner.

## Safer rollout
Prefer expand → migrate/backfill → verify → contract when old and new application versions may overlap. Make migrations idempotent where practical and resumable for large datasets.

## Recovery
Code rollback may not reverse a schema or data migration. Document whether recovery means rollback, restore, compensating migration, or forward fix. Destructive data operations require explicit human approval and verified recovery capability.
