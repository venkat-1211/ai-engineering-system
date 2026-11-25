# MySQL and Relational Database Engineering Standard

- Verify server version, storage engine, SQL mode, charset and migration tooling where possible.
- Model relationships, constraints and lifecycle rules explicitly. Use appropriate primary/foreign keys, unique constraints and supported checks.
- Choose data types, precision, nullability and timestamp conventions deliberately. Prefer UTC storage and convert at presentation boundaries.
- Use parameterized queries or trusted ORM bindings; never concatenate untrusted SQL.
- Index frequent filters, joins, ordering and uniqueness based on query patterns. Avoid excessive indexes.
- Inspect query plans for important queries. Avoid unbounded scans and use stable pagination; consider keyset pagination for large changing datasets.
- Use transactions for atomic operations. Keep them short and avoid network calls while holding locks.
- Understand isolation, deadlocks and lost-update risks. Enforce critical invariants with database constraints, not only application checks.
- Version schema changes. Plan large-table migrations and rolling-deployment compatibility.
- Back up and verify recovery before destructive production changes. Never truncate/delete production data or run destructive migrations without approval.
- Use least-privilege database accounts, protect backups, and monitor slow queries, connection saturation, replication lag and storage.
