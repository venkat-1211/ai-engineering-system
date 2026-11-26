# Agent Role Catalog

Use only roles relevant to the task. Role names describe responsibilities, not guaranteed built-in agents.

| Role | Primary responsibility | Typical deliverable | Must not |
|---|---|---|---|
| Orchestrator | Coordinate plan and integration | Orchestration plan, status, final report | Bypass approvals or fabricate evidence |
| Requirements analyst | Clarify user needs and acceptance criteria | Requirements and traceability | Implement before approval |
| Architect | Define boundaries and design | Design proposal, ADRs | Assume unverified stack details |
| Implementer | Deliver assigned change | Code/docs and change summary | Modify unassigned files |
| QA engineer | Validate expected behavior | Test plan and execution evidence | Report unrun tests as passed |
| Security reviewer | Assess security risks | Findings with severity and evidence | Expose secrets or exploit production |
| Independent reviewer | Review correctness and maintainability | Review findings | Rubber-stamp implementer claims |
| Database specialist | Review schema, queries, migrations | Data design and migration risks | Run destructive migrations without approval |
| API/integration specialist | Review contracts and external systems | API contract and integration tests | Call paid/live external systems without approval |
| CMS specialist | Review WordPress/OJS or other CMS constraints | Version-aware extension/theme review | Assume APIs/hooks without inspection |
| UX/accessibility specialist | Review usability and accessibility | UI findings and test scenarios | Change approved design scope silently |
| Release specialist | Assess release readiness | Release checklist and rollback plan | Deploy without explicit authorization |

## Role selection

Select roles by risk and technical surface, not by habit. A small isolated change may need one implementer and a lightweight review. A payment, authentication, personal-data, migration, or production-infrastructure change may require architecture, security, QA, and independent review.

## Independence

For high-risk work, reviewers should receive the requirements, relevant standards, and changed artifacts—not merely the implementer's conclusion. Reviewers should form their own assessment and identify evidence gaps.
