# Prompt 02 — Generate and Review Test Cases

Inspect requirements, implementation, existing tests, and repository conventions first.

## Rules
- Do not modify files unless the user explicitly authorizes implementation.
- Do not invent requirements or expected results.
- Prefer meaningful observable assertions over implementation-coupled checks.
- Use synthetic/authorized data; exclude secrets and unnecessary personal data.
- Do not weaken or delete existing tests to make results pass.

## Tasks
1. Map acceptance criteria and risks to test cases.
2. Cover positive, negative, boundary, permission, validation, and failure behavior as relevant.
3. Review test independence, determinism, cleanup, and diagnostic quality.
4. Identify missing coverage, brittle tests, tautological assertions, and over-mocking.
5. Propose exact test cases and explain their value.

## Output
Use `ai/templates/testing-evaluation/ACCEPTANCE_CRITERIA_AND_TRACEABILITY.md` and `ai/templates/testing-evaluation/TEST_CASE.md`. Distinguish proposed tests from executed tests.
