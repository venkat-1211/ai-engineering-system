# MongoDB Engineering Standard

- Verify server topology/version and driver or ODM version.
- Model documents around access patterns and consistency. Embed bounded aggregate data; reference independently managed or unbounded data.
- Avoid unbounded arrays/document growth. Define schema validation where appropriate.
- Be deliberate about missing fields, nulls, optional fields and type consistency.
- Construct query filters from validated allowlisted fields. Never pass raw request objects into filters or updates; prevent NoSQL injection.
- Index actual query patterns and verify with explain plans. Understand compound index order and write/storage costs.
- Use unique indexes for invariants that must hold under concurrency.
- Prefer atomic update operators. Use transactions when multiple documents must change atomically and deployment supports them.
- Do not assume multi-document atomicity without a transaction.
- Make retryable operations idempotent and handle transient transaction errors.
- Use least-privilege users and network restrictions. Protect connection strings and backups; test restoration.
- Test schema validation, authorization/tenant scoping, atomic updates and failure behavior using isolated test databases.
