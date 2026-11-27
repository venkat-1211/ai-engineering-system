# AI-Generated Code and Test Review

## Treat as a proposal
Generated code and tests are untrusted until reviewed. Verify that implementation matches requirements and local architecture, and that tests exercise real behavior.

## Review generated tests
Inspect assertions, fixtures, mocks, expected values, edge cases, authorization paths, cleanup, and failure behavior. Watch for tautological assertions, tests coupled to implementation, fabricated APIs, skipped checks, and mocks that hide integration defects.

## Independent verification
Run relevant tests yourself or inspect authentic execution output tied to the exact commit and environment. Review critical code paths independently of the agent that produced them.

## Security and privacy
Check generated fixtures, snapshots, logs, and examples for secrets and personal data. Review input handling, authorization, injection risks, deserialization, file access, and unsafe defaults.

## Reporting
Separate agent suggestions from verified facts. State what was inspected, what was executed, what failed, and what remains unverified.
