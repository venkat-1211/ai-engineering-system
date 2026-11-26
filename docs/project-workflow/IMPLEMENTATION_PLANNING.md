# Implementation Planning

## 1. Convert requirements into increments

Break the solution into small, ordered increments that can be reviewed and verified independently. Each task should state:
- Requirement/acceptance criteria addressed.
- Intended behavior and scope.
- Components/files likely affected (after repository discovery).
- Dependencies and prerequisites.
- Security/data/API implications.
- Tests and verification evidence required.
- Risks and rollback/recovery considerations.

Avoid over-specifying exact files before inspecting the repository.

## 2. Suggested sequencing

Adapt to the project; a common sequence is:
1. Confirm requirements and repository facts.
2. Resolve architecture and data/API contracts.
3. Add or update migrations and domain rules.
4. Implement server-side behavior and authorization.
5. Implement UI/client behavior.
6. Add integrations/background processing.
7. Add automated and manual tests.
8. Update documentation, configuration, and operational notes.
9. Perform independent review and release preparation.

Do not force this order if the architecture requires a different sequence. Explain material deviations.

## 3. Task sizing and dependencies

Prefer tasks that:
- Have a clear outcome.
- Can be completed and verified without unrelated work.
- Minimize cross-cutting changes.
- Have explicit prerequisites.
- Can be reviewed in a reasonable diff.

Identify critical dependencies, parallelizable work, shared-file conflicts, and integration points. Parallel agents must not edit overlapping files or shared interfaces without coordination.

## 4. Definition of done

A task is done only when:
- Its acceptance criteria are met.
- Implementation follows repository and applicable technology standards.
- Authorization, validation, and failure behavior are covered where relevant.
- Tests/checks were actually run and results recorded.
- Existing behavior and regression risk were reviewed.
- Documentation/configuration is updated where needed.
- Diff is focused and contains no accidental changes.
- Remaining risks and uncompleted work are disclosed.

## 5. Plan changes

When new information changes scope, estimates, architecture, or risk:
- Stop the affected work.
- Explain the discovery and impact.
- Update requirements, decisions, and plan.
- Obtain approval for material scope/cost/risk changes.
- Resume from the revised plan.
