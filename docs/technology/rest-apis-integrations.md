# REST APIs and Third-Party Integration Standard

- Define resource names, methods, status codes, validation errors and response shapes consistently.
- Validate path, query, header and body input. Do not use GET for state changes.
- Define pagination, filtering, sorting, authentication, authorization, rate limits and versioning.
- Avoid exposing internal models, secrets or unnecessary personal data.
- Authenticate and authorize every operation; enforce tenant/ownership boundaries.
- Set connection/response timeouts and verify TLS. Validate destination URLs and prevent SSRF; use allowlists where appropriate.
- Handle non-success responses, malformed payloads and timeouts.
- Retry only retryable operations with bounded backoff/jitter. Do not blindly retry non-idempotent actions.
- Use idempotency keys or reconciliation for payments, bookings and other high-impact operations.
- Verify webhook signatures using provider-documented methods and raw bytes where required. Reject invalid signatures.
- Apply timestamp/replay protection where supported. Persist event IDs and process duplicates idempotently.
- Handle out-of-order delivery and provider retries. Acknowledge quickly and queue longer work when appropriate.
- Never treat a client redirect as proof of payment success.
- Log safe correlation IDs, status and latency; redact secrets and personal data.
- Test timeouts, duplicate events, invalid signatures, replay and provider errors.
