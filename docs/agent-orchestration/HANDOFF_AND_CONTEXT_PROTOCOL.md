# Handoff and Context Protocol

## Handoff purpose

A handoff transfers enough verified context for another agent to continue without guessing. It is not a transcript dump.

## Required handoff fields

- task ID, title, owner, status;
- objective and acceptance criteria;
- relevant repository paths and instructions read;
- scope and explicit exclusions;
- files created or modified;
- key implementation/design decisions and rationale;
- commands actually executed;
- tests and checks with exact outcomes;
- unresolved issues, assumptions, and risks;
- required next action and receiving owner;
- approval still required, if any.

Use `ai/templates/agent-orchestration/HANDOFF_REPORT.md`.

## Evidence language

Distinguish:
- **Observed:** directly inspected or executed.
- **Inferred:** reasoned from observed evidence.
- **Assumed:** not yet verified.
- **Not run:** not executed.
- **Blocked:** could not proceed and why.

Never convert an assumption into a fact during handoff.

## Context minimization

Provide the next agent with the relevant source files, applicable standards, task card, decisions, and evidence. Avoid unrelated conversation history, duplicate instructions, and large raw logs unless needed.

## Receiving-agent duties

The receiving agent must:
1. read the handoff and relevant repository instructions;
2. verify critical assumptions and current file state;
3. confirm ownership and permissions;
4. identify missing context before acting;
5. report conflicts or stale information to the orchestrator.

Do not assume shared memory or shared tool state unless the environment explicitly confirms it.
