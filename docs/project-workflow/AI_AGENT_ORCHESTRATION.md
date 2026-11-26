# AI Agent Orchestration

## 1. Principles

- One clearly identified owner coordinates the task and maintains the source of truth.
- Agents receive bounded responsibilities, relevant context, and explicit deliverables.
- Separate implementation from independent review for high-risk work.
- Do not ask multiple agents to modify the same files concurrently.
- Treat agent output as untrusted until inspected, tested, and reviewed.
- Human approval remains mandatory for actions outside delegated authority.

## 2. Suggested roles

| Role | Responsibility | Must not |
|---|---|---|
| Coordinator / lead | Clarify scope, maintain plan, resolve conflicts, integrate work | Claim work was verified without evidence |
| Requirements analyst | Identify actors, workflows, rules, acceptance criteria | Invent stakeholder decisions |
| Architect | Inspect stack, propose boundaries and trade-offs | Force a preferred technology without evidence |
| Implementer | Make bounded code changes and tests | Expand scope or bypass gates |
| QA engineer | Derive and execute tests, report defects | Mark unexecuted tests as passed |
| Security reviewer | Review threats, authorization, secrets, dependencies, abuse cases | Assume prompts alone enforce security |
| Release owner | Review rollout, backup, rollback, monitoring | Deploy without required approval |

One agent may perform multiple roles on a small task. For high-risk work, use an independent reviewer who did not author the implementation.

## 3. Task handoff contract

Every agent handoff should include:
- Goal and background.
- Relevant requirements and acceptance criteria.
- Repository facts and applicable standards.
- Exact scope and files/components allowed to change.
- Files or areas explicitly out of scope.
- Constraints, assumptions, and open questions.
- Required tests/reviews.
- Permission boundaries.
- Expected output format and evidence.

The receiving agent should report its understanding and blockers before making broad changes.

## 4. Context management

Provide the smallest sufficient context:
- Root `AGENTS.md` and applicable tool instructions.
- Relevant technology standards.
- Requirements, ADRs, API/data contracts.
- Relevant source files and tests.
- Recent decisions and unresolved issues.

Do not assume an agent has read a file or remembers another agent's conversation. Put durable decisions in repository artifacts.

## 5. Parallel work

Parallelize independent tasks only. Before parallel execution:
- Define ownership by module/file/interface.
- Agree contracts and integration points.
- Avoid concurrent edits to shared files.
- Specify how conflicts and partial failures are handled.
- Integrate and test the combined result.

## 6. Independent review

Reviewers should inspect the actual diff and evidence, not only the implementer's summary. Review:
- Requirement coverage and scope.
- Security and authorization.
- Data/API compatibility.
- Error handling and edge cases.
- Test quality and execution.
- Performance and operational effects.
- Accidental changes and maintainability.

Record findings by severity, file/location, impact, and recommended correction. Do not claim a clean review if it was not performed.
