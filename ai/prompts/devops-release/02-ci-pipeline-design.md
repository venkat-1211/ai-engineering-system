# Prompt 02 — Design a Secure CI Pipeline

Design a CI pipeline for the identified stack and repository. First inspect existing workflows and project instructions. Preserve current behavior unless a documented defect requires a proposed change.

Include stages for checkout, policy/syntax validation, locked dependency install, tests, static analysis, security/secret/dependency scanning, build, artifact digest, and evidence publication. Define permissions per job, runner trust boundaries, caching rules, concurrency, timeouts, fork/PR isolation, and failure behavior.

Return proposed file changes as complete files or a patch plan. Do not invent test results. Do not add deployment or production credentials to CI. Ask for human approval before modifying repository files if the user has not authorized implementation.
