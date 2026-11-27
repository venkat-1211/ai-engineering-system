# Stage 9 AGENTS.md Addendum — Testing, Evaluation & Quality Assurance (Merged)

> **Status:** Reference-only historical aid (Merged). The concise governing rules below have been selectively integrated into the existing root `AGENTS.md`. Root `AGENTS.md` remains the single active root instruction file; do not treat this addendum as a replacement for or authority above `AGENTS.md`.

## Required governing rules
- Define observable acceptance criteria and a risk-based verification plan before making material changes.
- Select test levels and non-functional checks proportionate to impact, exposure, complexity, and failure cost.
- Treat test output, coverage, static-analysis output, screenshots, and agent claims as evidence only for the exact scope actually checked.
- Never claim a test passed unless it was executed successfully; report `Passed`, `Failed`, `Not run`, `Blocked`, or `Requires human approval` accurately.
- AI-generated code and AI-generated tests require independent review for correctness, meaningful assertions, security, edge cases, and false confidence.
- Do not silently skip, delete, weaken, quarantine, or rewrite failing tests. Explain the reason, impact, owner, and approval where applicable.
- Keep test data synthetic or properly authorized and sanitized; never expose secrets or unnecessary personal data in fixtures, logs, screenshots, or reports.
- Record the commit, environment, configuration, commands, results, limitations, and residual risks for material verification.
- Do not treat code coverage or a green pipeline as proof of correctness, security, performance, or release readiness.
- Require authorized human approval for release exceptions and other decisions designated high impact by project policy.

## Suggested integration locations
Integrate these rules into existing `AGENTS.md` sections governing workflow, quality/testing, security, completion evidence, and release/operations. Preserve all existing sections, precedence rules, and Stages 1–8. Avoid duplicate policy text; link to `docs/testing-evaluation/README.md` for detailed guidance.
