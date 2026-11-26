# Stage 5 Addendum — Reference-Only Integration Aid (Merged)

> **Reference-only integration aid.** The applicable Stage 5 guidance from this file has already been selectively integrated into the root `AGENTS.md`. This file is not a second active root instruction file and must not replace `AGENTS.md`; root `AGENTS.md` remains the single active root instruction file.

## Suggested net-new root guidance

### Multi-agent coordination

For tasks involving multiple AI agents, use `docs/agent-orchestration/README.md` and the applicable orchestration standards. Multi-agent execution is optional; use a single agent for small, isolated tasks when that is simpler and safer.

### Ownership and coordination

Assign one accountable owner to every task and designate one orchestrator to maintain the consolidated plan, dependencies, decisions, and status. Agents must work only within their assigned scope and permissions. The orchestrator coordinates; it does not silently grant permissions or bypass human approval.

### Parallel execution

Parallelize only tasks whose dependencies and write scopes are understood. Assign explicit file or component ownership. Avoid concurrent edits to the same files unless the tool provides a verified merge/conflict-control workflow. Integrate parallel outputs through review and tests.

### Handoffs and verification

Use the Stage 5 task-card and handoff templates. Handoffs must include scope, files touched, decisions, commands actually run, test results, known limitations, and remaining work. Treat unverified claims as unverified. High-risk changes require independent review in accordance with existing Stage 3 and Stage 4 gates.

### Existing policies remain authoritative

Stage 5 does not override instruction precedence, security rules, Git safety, technology standards, lifecycle gates, or human-approval requirements from Stages 1–4. Agents must not perform destructive, production, paid, externally visible, or sensitive actions without the approvals required by the existing standards.
