# Multi-Agent Operating Model

## Roles in the operating model

A multi-agent team is a logical assignment of responsibilities. It does not imply that the IDE or model can launch agents, share context, or execute tasks concurrently. Verify the capabilities of the actual tool.

- **Orchestrator:** owns the plan, assignments, dependencies, decisions, integration, and consolidated report.
- **Architect:** evaluates requirements, boundaries, design options, and architecture decisions.
- **Implementer:** changes only assigned code or documentation within the task scope.
- **QA / test agent:** derives test scenarios, runs permitted checks, and reports evidence.
- **Security reviewer:** assesses threats, trust boundaries, authorization, data handling, and vulnerabilities.
- **Independent reviewer:** reviews implementation against requirements and standards without relying on implementer assertions.
- **Domain specialist:** provides focused expertise such as database, API, CMS, frontend, infrastructure, or accessibility.

One agent may hold multiple roles on low-risk work. For high-risk work, separate implementation and independent review where feasible.

## Accountability

Every task has exactly one accountable owner. Contributors may assist, but the owner is responsible for the task card, status, evidence, and handoff.

The orchestrator:
- assigns tasks and records owners;
- confirms dependencies and file ownership;
- checks that agents have sufficient but not excessive context;
- prevents scope expansion;
- resolves or escalates conflicts;
- integrates outputs and verifies completion.

The orchestrator must not mark work complete without evidence.

## Responsibility boundaries

Agents must not:
- silently expand their assigned scope;
- overwrite another agent's work;
- assume another agent's tests passed;
- grant themselves or others additional permissions;
- approve their own high-risk work as the only reviewer;
- claim a command, test, deployment, or inspection occurred when it did not.

## Single-agent fallback

If the environment does not support multi-agent execution, use the same roles sequentially as review perspectives, clearly label simulated role changes, and do not claim that separate agents were run.
