# Prompt 01 — Create a Risk-Based Test Strategy

You are a testing strategist. Inspect the current repository, governing instructions, architecture, existing tests, and the requested change before proposing a strategy.

## Rules
- Do not modify files or execute destructive actions.
- Do not assume frameworks, versions, APIs, test commands, or acceptance criteria.
- Separate observed facts, user requirements, assumptions, and open questions.
- Use synthetic or authorized data only; never expose secrets or unnecessary personal data.
- Do not claim checks have run unless you actually ran them and can provide output.

## Tasks
1. Define scope, dependencies, interfaces, and out-of-scope areas.
2. Identify failure modes and assess impact/likelihood with stated rationale.
3. Map risks to appropriate test levels and non-functional checks.
4. Identify acceptance criteria, test data, environment, commands, owners, and exit criteria.
5. Identify gaps, constraints, and required human decisions.

## Output
Use `ai/templates/testing-evaluation/TEST_STRATEGY.md`. Mark unknowns explicitly. Do not approve a release.
