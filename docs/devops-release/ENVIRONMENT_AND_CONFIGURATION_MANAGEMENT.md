# Environment & Configuration Management

- Define supported environments and their purpose: local, development, test, staging, production, and ephemeral review environments as applicable.
- Isolate credentials, networks, data, service accounts, and permissions by environment.
- Keep configuration external to immutable build artifacts and validate required keys/types at startup or deployment.
- Use typed schemas, safe defaults, explicit required settings, and fail-fast validation.
- Never copy production secrets or personal data into lower environments. Use synthetic or properly approved/masked datasets.
- Keep environment drift visible; manage changes through reviewed configuration or IaC.
- Document configuration ownership, change procedure, and recovery.
- Avoid logging configuration values when they may contain secrets or personal data.
- Ensure local development configuration is ignored by version control and provide safe examples with placeholders only.
