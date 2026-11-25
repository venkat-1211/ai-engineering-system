# AI-Assisted Development Workflow

Use this workflow for features, bug fixes, refactoring and technical changes.

## Step 0 — Protect the working state
- Inspect version-control status.
- Identify user changes and do not overwrite them.
- Confirm the working branch and target environment.
- Do not access production or perform destructive actions without approval.

## Step 1 — Understand
Ask the agent to inspect relevant code, documentation, configuration and tests. Require a concise summary of the current implementation and discovered conventions.

**Gate:** Do not implement until the task and scope are understood.

## Step 2 — Specify
Write:
- Problem statement.
- In-scope and out-of-scope items.
- Acceptance criteria.
- Business rules.
- Validation and authorization requirements.
- Edge cases and failure behavior.
- Compatibility constraints.

Separate confirmed facts from assumptions.

**Gate:** Obtain clarification or approval for material ambiguities.

## Step 3 — Plan
Ask for:
- Proposed design.
- Files likely to change.
- Data/API contract changes.
- Security implications.
- Test plan.
- Risks and rollback considerations.

For small, low-risk changes, a brief plan is sufficient. For high-risk or cross-cutting changes, require explicit review.

## Step 4 — Implement incrementally
- Make one coherent change at a time.
- Avoid unrelated cleanup.
- Add tests with the behavior.
- Keep changes small enough to review.
- Stop and report if implementation reveals a conflicting requirement or unsafe assumption.

## Step 5 — Verify
Discover and run relevant repository commands:
- Tests.
- Lint/format checks.
- Static analysis/type checks.
- Build checks.
- Targeted manual or browser verification where relevant.

Capture actual outcomes. Do not claim success for checks not run.

## Step 6 — Independent review
Use a separate review pass or reviewer agent to inspect:
- Requirement coverage.
- Logic and edge cases.
- Security and authorization.
- Data integrity and concurrency.
- Performance.
- Maintainability.
- Unintended scope changes.

Reviewers should report findings before modifying code. Fix findings in a separately reviewable pass.

## Step 7 — Final diff and handoff
Inspect the final diff for:
- Unrelated changes.
- Accidental secrets or sensitive data.
- Debug code and temporary files.
- Missing tests or documentation.
- Destructive or breaking behavior.

Provide the completion report required by `AGENTS.md`.

## Risk-based approval

Always obtain explicit approval before:
- Deleting or overwriting user data.
- Running destructive database operations.
- Changing authentication or authorization behavior materially.
- Weakening security controls.
- Installing a new dependency with material risk.
- Changing public APIs or data contracts incompatibly.
- Accessing production systems or data.
- Deploying, publishing or triggering paid external operations.

## Suggested task prompt

> Read `AGENTS.md` and the referenced standards. Inspect the existing implementation and tests before changing anything. For this task, first report the relevant current behavior, acceptance criteria, proposed files to change, risks and test plan. Do not edit files until I approve the plan. After approval, implement in small steps, run the relevant checks, inspect the final diff and report only verified results.
