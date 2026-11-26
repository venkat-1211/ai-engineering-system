# Data, API, and Integration Design

## 1. Data design

For schema or data changes, define:
- Entities, ownership, relationships, and identifiers.
- Required/optional fields, types, constraints, defaults, and indexes.
- Uniqueness, referential integrity, and lifecycle.
- Sensitive data classification, access, encryption, retention, and deletion.
- Audit/history requirements.
- Expected data volume, query patterns, and growth.
- Transaction boundaries, concurrency, and consistency.
- Migration/backfill strategy and compatibility with deployed versions.

Migration safety:
- Review existing data before applying assumptions.
- Prefer additive, backward-compatible changes where possible.
- Plan large backfills separately from schema changes.
- Consider locks, downtime, batch size, retries, and resumability.
- Define validation and reconciliation after migration.
- Provide backup and recovery/rollback strategy.
- Do not run destructive or production migrations without explicit approval.

## 2. API contract design

Define as applicable:
- Resource names and HTTP methods.
- Request/response schemas and content types.
- Authentication and authorization.
- Validation rules and field constraints.
- Status codes and stable error format.
- Pagination, filtering, sorting, and limits.
- Idempotency and concurrency behavior.
- Rate limiting and abuse protection.
- Versioning and backward compatibility.
- Deprecation and migration policy.
- Logging, tracing, and sensitive-field redaction.

Never rely only on frontend checks for authorization or data integrity. Enforce access control and validation on the trusted server side.

## 3. Integration design

For each external or internal integration, record:
- System owner and purpose.
- Authentication method and secret storage.
- Network direction and allowed origins/endpoints.
- Timeouts, retries, backoff, and circuit-breaking behavior where appropriate.
- Idempotency and duplicate event handling.
- Webhook signature verification and replay protection.
- Rate limits and provider quotas.
- Failure behavior and user-visible status.
- Monitoring, alerting, and reconciliation.
- Sandbox/test environment and production approval process.

Do not log tokens, passwords, personal data, payment data, or full sensitive payloads.

## 4. Compatibility review

Check compatibility with:
- Existing clients and consumers.
- Deployed application versions.
- Database schema and data.
- External providers.
- Browser/device/API consumers.
- Queue/event payloads and background workers.

For breaking changes, define a coordinated migration and deprecation plan rather than silently changing the contract.
