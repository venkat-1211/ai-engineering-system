# Node.js and Express Engineering Standard

- Verify Node.js, Express, module system and package manager versions.
- Separate routing, validation, handlers, business logic and infrastructure according to project complexity.
- Keep handlers focused on HTTP. Use centralized error handling and stable response contracts.
- Validate path, query, header and body input; enforce size and content-type limits.
- Use allowlists for accepted fields. Do not pass raw request objects into database filters or updates.
- Authenticate and authorize every protected operation; enforce tenant/ownership boundaries in data access.
- Configure secure headers, explicit CORS and rate limits. Never combine wildcard CORS with credentialed requests.
- Configure cookies and CSRF defenses according to the authentication model.
- Propagate async errors. Set timeouts; bound retries and concurrency; avoid CPU-heavy event-loop blocking.
- Make retryable operations idempotent. Implement graceful shutdown and close database/queue connections.
- Validate uploads and protect against injection, path traversal and unsafe deserialization.
- Keep secrets in protected configuration. Redact tokens, cookies and personal data from logs.
- Use connection pooling, health/readiness checks and structured redacted logs.
- Test middleware, authorization, validation, errors, integration boundaries and shutdown behavior where critical.
