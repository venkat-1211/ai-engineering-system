# Test Data and Environment Management

## Data safety
Prefer synthetic data. Use production-derived data only when explicitly authorized, minimized, sanitized, access-controlled, and handled under applicable project policy. Never place secrets, credentials, tokens, or unnecessary personal data in fixtures.

## Isolation
Give each test or run a predictable data namespace. Reset or clean state safely. Prevent tests from touching production services or shared environments unintentionally.

## Environment fidelity
Record meaningful differences between test and production: versions, feature flags, topology, permissions, integrations, and configuration. Do not claim production behavior is verified when the environment differs materially.

## Secrets and configuration
Inject test credentials through approved secret handling. Use least privilege, short-lived credentials where possible, and safe redaction. Do not print secrets in logs or reports.

## Repeatability
Document setup, seed data, dependencies, and cleanup. Avoid tests that require undocumented manual state. Ensure parallel execution cannot corrupt shared data.
