# Stage 9 — AI Engineering Testing, Evaluation & Quality Assurance

## Purpose
Establish a repeatable, evidence-based quality system for software changes and AI-assisted engineering. This stage covers test strategy, test design, automated and manual verification, AI-generated code review, agent and prompt evaluation, regression control, defect management, and release-quality evidence.

## Scope
- Risk-based verification planning and test strategy
- Requirements-to-tests traceability and acceptance criteria
- Unit, integration, contract, end-to-end, accessibility, security, performance, and resilience testing
- Test data, environments, isolation, determinism, and cleanup
- AI-generated code verification and independent review
- Agent, prompt, and model evaluation where applicable
- Regression suites, flaky-test management, and defect triage
- Quality gates, coverage interpretation, and release evidence

## Repository map
- `docs/testing-evaluation/` — standards and operating guidance
- `ai/templates/testing-evaluation/` — reusable quality records
- `ai/checklists/testing-evaluation/` — verification checklists
- `ai/prompts/testing-evaluation/` — controlled assessment prompts
- `AGENTS.md` — governing integration points

## Operating principles
1. Quality is demonstrated by relevant evidence, not by confidence, code volume, or a passing badge alone.
2. Choose test depth based on impact, likelihood, complexity, exposure, and reversibility.
3. Tests must verify observable requirements and failure behavior, not merely implementation details.
4. A test that was not run must never be reported as passed.
5. AI-generated code and AI-generated test cases require independent scrutiny.
6. Test results are scoped to the exact commit, environment, configuration, and data used.
7. Do not weaken, skip, delete, or rewrite tests merely to obtain a green result without an approved, documented reason.
8. Human approval remains required for high-impact release decisions where policy or risk requires it.

## Recommended adoption sequence
1. Read `docs/testing-evaluation/README.md`.
2. Establish risk, acceptance criteria, and verification scope before implementation.
3. Create a test strategy and traceability record for meaningful changes.
4. Run targeted tests, then appropriate regression and non-functional checks.
5. Review AI-generated implementation and tests independently.
6. Record failures, skipped checks, limitations, and residual risks.
7. Apply the quality gate before release or handoff.

## Boundaries
This stage defines engineering practices; it does not claim that a repository has been tested, that a system is defect-free, or that any external standard or certification has been met. Actual execution evidence must come from the current project and environment.
