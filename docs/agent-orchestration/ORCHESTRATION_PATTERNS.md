# Orchestration Patterns

Choose the simplest pattern that meets the task's risk and coordination needs.

## 1. Sequential specialist review

Flow: analyst → architect → implementer → QA → independent reviewer.

Use when decisions depend on earlier outputs or shared files are involved. It is the safest default for tightly coupled work.

## 2. Parallel research, centralized synthesis

Several agents independently investigate non-overlapping questions; the orchestrator compares evidence and creates one consolidated design.

Use for repository discovery, technology research, threat modeling, or options analysis. Research agents should not make competing edits.

## 3. Parallel implementation by bounded ownership

Agents implement separate modules or files with explicit interfaces and non-overlapping write scopes. Integrate only after contract agreement.

Use only when tasks are genuinely independent and shared interfaces are stable. If overlap is unavoidable, serialize the edits.

## 4. Implementer plus independent reviewer

One agent implements; another reviews requirements coverage, security, tests, and maintainability. A third QA role may execute validation.

Use for changes where independent verification materially reduces risk.

## 5. Specialist consultation

A domain specialist returns advice or a focused artifact; the accountable implementer retains ownership of the final change.

Use for database, security, CMS, API, performance, or accessibility questions.

## Pattern selection rules

- Do not parallelize a task merely to use more agents.
- Do not parallelize tasks with unresolved shared-interface decisions.
- Do not ask multiple agents to edit the same file concurrently.
- Use sequential execution when a task has a strict dependency chain.
- Keep one orchestrator responsible for synthesis and final status.
- Record why a chosen pattern is appropriate for medium/high-risk work.
