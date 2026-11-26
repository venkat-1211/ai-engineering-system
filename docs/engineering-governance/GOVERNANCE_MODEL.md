# Governance Model

## 1. Purpose and scope

Define how engineering policies, risks, control decisions, exceptions, and improvement activities are governed. Tailor the model to the actual organization and project.

## 2. Governance layers

- **Organization or portfolio:** risk appetite, policy ownership, legal/compliance advice, shared standards.
- **Project or product:** project-specific risks, stakeholders, data, architecture, quality objectives, release decisions.
- **Delivery team:** implementation evidence, test outcomes, code review, operational readiness, issue escalation.
- **AI agent activity:** bounded tasks, declared assumptions, traceable outputs, human review where required.

A small project may combine roles, but must not silently remove accountability or required independent review.

## 3. Decision classes

| Decision | Minimum accountable authority |
|---|---|
| Routine implementation within approved scope | Assigned engineering owner |
| Architecture or material scope change | Designated technical decision owner |
| Risk acceptance | Authorized human risk owner |
| Compliance interpretation | Qualified organizational/legal/compliance authority as appropriate |
| Production release | Authorized release owner |
| Security exception | Authorized security/risk owner |
| Data access or external disclosure | Data owner or authorized approver |

Actual authority must be confirmed from the organization. Do not assume a role title grants permission.

## 4. Risk-based depth

Consider impact, likelihood, exposure, reversibility, affected users, data sensitivity, and detectability. Higher-impact systems require stronger review, evidence, monitoring, and escalation.

## 5. Governance records

Maintain only records relevant to the project:
- governance charter and role assignments;
- risk register and decisions;
- compliance applicability and evidence register;
- policy versions and approvals;
- exceptions and waivers;
- quality scorecards;
- audit evidence index;
- improvement action plans.

## 6. AI agent boundaries

AI agents can prepare assessments, identify gaps, summarize evidence, and recommend controls. They cannot independently accept organizational risk, approve legal interpretations, grant themselves permissions, attest to compliance, or authorize production actions.

## 7. Review and change

Review governance after material changes to intended use, architecture, data, dependencies, threat environment, applicable obligations, ownership, or deployment. Define a periodic cadence appropriate to risk.
