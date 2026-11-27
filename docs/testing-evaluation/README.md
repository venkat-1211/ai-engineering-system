# Testing, Evaluation & Quality Assurance

## Objective
Provide a practical quality framework for software and AI-assisted engineering work. Verification should reduce meaningful risk and produce reproducible evidence.

## Quality lifecycle
1. **Understand** — inspect current instructions, repository, architecture, dependencies, and existing tests.
2. **Specify** — translate requirements into observable acceptance criteria, including negative and failure cases.
3. **Plan** — identify risks, test levels, data, environments, tools, owners, and exit criteria.
4. **Design** — build tests that are independent, deterministic where feasible, maintainable, and meaningful.
5. **Execute** — run targeted checks, inspect results, investigate failures, then run appropriate regression checks.
6. **Evaluate** — review implementation and tests independently, including AI-generated artifacts.
7. **Decide** — assess evidence, gaps, residual risk, and required approvals.
8. **Learn** — record defects, escaped issues, flaky tests, and improvements.

## Test status vocabulary
Use exactly: `Passed`, `Failed`, `Not run`, `Blocked`, `Requires human approval`. Include a short reason for every status other than Passed. Do not convert skipped or blocked checks into success.

## Risk-based test selection
Consider business impact, likelihood, blast radius, data sensitivity, security exposure, integration complexity, novelty, and rollback difficulty. High-risk changes generally need multiple complementary test levels and independent review. Low-risk changes may use a smaller targeted set with a stated rationale.

## Evidence requirements
For material changes record repository/commit, environment, runtime and dependency versions where relevant, configuration, test command, timestamp/time zone where available, result, failures, skipped checks, and limitations. Preserve enough output or links for another engineer to verify the claim. Never fabricate evidence.

## Test quality
A useful test has a clear purpose, meaningful setup, action, and assertion. It should fail when the behavior is wrong, avoid dependence on execution order, isolate state, and clean up resources. Prefer observable behavior over brittle internal implementation details.

## AI-assisted work
Treat generated code, test cases, test plans, and evaluation summaries as untrusted proposals until inspected and verified. Check test oracles, edge cases, security implications, and whether the test actually detects the intended defect. An agent's assertion that tests passed is not evidence without actual output.

## Related guidance
- `docs/testing-evaluation/TEST_STRATEGY_AND_RISK.md`
- `docs/testing-evaluation/REQUIREMENTS_AND_TRACEABILITY.md`
- `docs/testing-evaluation/TEST_DESIGN_AND_ASSERTIONS.md`
- `docs/testing-evaluation/TEST_LEVELS_AND_PYRAMID.md`
- `docs/testing-evaluation/TEST_DATA_AND_ENVIRONMENTS.md`
- `docs/testing-evaluation/AUTOMATION_AND_CI_QUALITY_GATES.md`
- `docs/testing-evaluation/AI_GENERATED_CODE_AND_TEST_REVIEW.md`
- `docs/testing-evaluation/AGENT_PROMPT_AND_MODEL_EVALUATION.md`
- `docs/testing-evaluation/REGRESSION_AND_FLAKY_TEST_MANAGEMENT.md`
- `docs/testing-evaluation/DEFECT_TRIAGE_AND_ROOT_CAUSE.md`
- `docs/testing-evaluation/NON_FUNCTIONAL_QUALITY_TESTING.md`
- `docs/testing-evaluation/QUALITY_EVIDENCE_AND_RELEASE_GATES.md`
