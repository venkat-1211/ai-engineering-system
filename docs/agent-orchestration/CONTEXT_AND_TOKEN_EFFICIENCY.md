# Context and Token Efficiency

## Objective

Reduce repeated context and irrelevant output without omitting information required for correctness, security, or traceability.

## Context packet

For each agent, provide:
- task objective and acceptance criteria;
- assigned role and accountable owner;
- allowed scope and permissions;
- relevant repository instructions and technology standards;
- necessary files and interfaces;
- dependency status and prior decisions;
- required output format and evidence expectations.

## Efficiency practices

- Link to authoritative repository documents instead of copying long standards into every prompt.
- Send only task-relevant files and bounded excerpts.
- Summarize prior work with evidence and unresolved questions.
- Keep one decision log rather than repeating decision history in every handoff.
- Ask agents for concise, structured outputs.
- Avoid duplicate research unless independent verification is intentional.
- Do not truncate security requirements, acceptance criteria, or critical constraints to save tokens.

## Context refresh

Before continuing a long-running task, verify current repository state, branch, changed files, task status, and whether prior assumptions remain valid. A stale summary is not authoritative over current files.

## Quality over token count

Never omit necessary tests, security review, error handling, or user approval to reduce token usage.
