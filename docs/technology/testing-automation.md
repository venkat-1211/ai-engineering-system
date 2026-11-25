# Testing and Automation Engineering Standard

Choose tools already configured by the project. Do not impose a new test framework without approval.

- Use unit tests for isolated rules, integration tests for infrastructure boundaries, feature/API tests for service behavior, UI tests for interactions, E2E tests for critical workflows and contract tests for important integrations.
- Prioritize authentication, authorization, tenant isolation, validation, business invariants, transactions, concurrency, duplicate requests, file access, payments and webhooks.
- Test observable behavior rather than mirroring implementation details.
- Keep tests deterministic, isolated and repeatable. Use controlled fakes/sandboxes instead of live third-party services in normal tests.
- Never use production credentials/data. Ensure tests clean up resources.
- Include negative, boundary, failure and authorization cases.
- Inspect test configuration before commands that reset databases, truncate tables, drop schemas or modify files. Verify test targets are isolated.
- Never run destructive tests against production/shared systems. Never weaken tests to make CI green.
- Report exact commands executed and results. Distinguish local checks, CI results and manual checks.
- Where CI exists, use repeatable lint/format, static analysis/type-check, tests, build and dependency/security gates. Do not claim a gate exists unless configured.
