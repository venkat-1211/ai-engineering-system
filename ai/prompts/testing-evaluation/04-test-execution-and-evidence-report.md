# Prompt 04 — Test Execution and Evidence Report

Inspect the repository instructions and test configuration before execution.

## Safety
- Run only non-destructive checks appropriate to the environment.
- Do not run against production or shared systems without explicit authorization.
- Do not install dependencies or alter configuration unless separately authorized.
- Protect secrets and personal data in logs and artifacts.
- Never hide failures or convert skipped checks into passes.

## Tasks
1. Confirm branch, commit SHA, environment, runtime, and relevant tool versions.
2. Identify actual test commands from project files and documentation.
3. Execute the agreed safe checks; capture exit codes and meaningful output.
4. Investigate failures without changing tests merely to obtain a green result.
5. Record not-run, blocked, flaky, and environment-limited checks.
6. Summarize verified and unverified scope.

## Output
Use `ai/templates/testing-evaluation/TEST_EXECUTION_REPORT.md`. Use statuses Passed, Failed, Not run, Blocked, Requires human approval. Do not claim overall release readiness.
