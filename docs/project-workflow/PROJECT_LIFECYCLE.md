# Project Lifecycle and Approval Gates

## 1. Principles

- Deliver user and business value with correctness, security, reliability, maintainability, and measurable quality.
- Establish the problem before selecting a technology or writing code.
- Prefer evidence from the repository and stakeholders over assumptions.
- Use the least complex design that satisfies known requirements and foreseeable constraints.
- Make decisions visible and reversible where practical.
- Scale process to risk, uncertainty, blast radius, and regulatory or contractual obligations.

## 2. Lifecycle

### Gate 0 — Intake and discovery

Capture the request, requester/stakeholders, affected users, problem, expected outcome, urgency, constraints, and known systems involved.

Inspect the repository before estimating implementation. Identify:
- Application type and architecture.
- Languages, frameworks, versions, package managers, and lockfiles.
- CMS platforms (such as WordPress and Open Journal Systems (OJS)), CMS and plugin/theme versions, theme/plugin/extension/customization boundaries, and existing CMS APIs, hooks, conventions, and compatibility constraints where present. Do not assume APIs or version-specific functionality; inspect the actual installed version and documentation.
- Database, migrations, queues, caches, storage, and external services.
- Authentication, authorization, roles, and sensitive data.
- Build, test, CI/CD, deployment, and observability setup.
- Existing behavior and relevant tests.

**Exit:** The problem is understood well enough to write requirements or ask specific questions. Unknowns are recorded.

### Gate 1 — Requirements and scope

Define:
- Goals and measurable outcomes.
- Users, actors, and relevant user journeys.
- Functional requirements.
- Non-functional requirements: security, privacy, performance, availability, accessibility, compatibility, scalability, operability, and maintainability as relevant.
- In-scope and out-of-scope items.
- Business rules, validation, permissions, failure states, and edge cases.
- Data classification, retention, audit, and compliance needs where applicable.
- Assumptions, dependencies, constraints, and open questions.
- Acceptance criteria that can be verified.

Avoid ambiguous terms such as “fast”, “secure”, “user-friendly”, or “fully responsive” without defining how they will be evaluated.

**Exit:** Scope and acceptance criteria are sufficiently clear and agreed by the appropriate owner. Unresolved high-impact questions block implementation.

### Gate 2 — Solution design

Discover and compare viable approaches. Define architecture boundaries, components, data flow, trust boundaries, integrations, data model, API contracts, error handling, observability, and deployment implications.

Record material decisions and alternatives in an Architecture Decision Record (ADR). Perform threat/risk analysis for security-sensitive or high-impact work.

**Exit:** The proposed solution is feasible, compatible with the actual stack, and reviewed at a level appropriate to risk.

### Gate 3 — Delivery planning

Break work into ordered, independently verifiable increments. Identify dependencies, owners, risks, migrations, feature flags, test layers, rollout steps, and rollback/recovery.

Each task should map to one or more requirements and acceptance criteria. Avoid plans that are merely a list of files to edit.

**Exit:** Work is sequenced, dependencies and risks are understood, and verification is planned.

### Gate 4 — Implementation

Implement one coherent increment at a time. Follow repository conventions and applicable Stage 3 technology standards. Keep changes focused and reviewable.

For each increment:
1. State the intended requirement and files/components affected.
2. Make the smallest safe change.
3. Add or update tests.
4. Run relevant checks.
5. Review the diff for scope, security, and regressions.
6. Record remaining risks or follow-up work.

**Exit:** Each increment meets its acceptance criteria and has truthful verification evidence.

### Gate 5 — Verification and independent review

Run relevant automated and manual checks:
- Unit, integration, contract, end-to-end, regression, and migration tests as applicable.
- Static analysis, formatting, type checks, dependency/security scans where configured.
- Authorization, validation, error handling, and abuse-case checks.
- Responsive, accessibility, browser/device, performance, and reliability checks as applicable.
- Independent code/security review for high-risk changes.

A test is Passed only if it was actually executed and succeeded. Report Failed, Not run, Blocked, or Requires human approval accurately.

**Exit:** No unresolved release-blocking defect or risk remains, or an authorized owner explicitly accepts the documented risk.

### Gate 6 — Release and deployment

Before release, confirm:
- Approved scope and release owner.
- Build artifact and environment configuration.
- Secrets and access controls.
- Database migration and data compatibility plan.
- Backup/restore and rollback/recovery plan.
- Feature flags and staged rollout where appropriate.
- Monitoring, alerts, logs, and support ownership.
- Communication and maintenance window if required.
- Human approval for production-impacting actions.

Deploy using the established release process. Verify health and critical user journeys after deployment.

**Exit:** Release is verified, or rollback/recovery is initiated and communicated.

### Gate 7 — Operations and maintenance

Monitor reliability, errors, performance, security alerts, user feedback, and operational costs. Triage incidents and regressions. Track technical debt with impact and priority. Update documentation and runbooks when operational truth changes.

**Exit:** Ownership, support path, and follow-up actions are clear.

## 3. Risk-based depth

Use deeper design, testing, and approval for changes involving:
- Authentication, authorization, identity, sessions, or account recovery.
- Payments, financial records, or billing.
- Personal, confidential, regulated, or high-value data.
- Data deletion, bulk updates, schema changes, or migrations.
- Public APIs, third-party integrations, or externally visible behavior.
- Infrastructure, DNS, certificates, secrets, production access, or deployment.
- Security controls, cryptography, file uploads, or user-generated content.
- High-availability, safety-critical, or business-critical workflows.

For low-risk changes, concise requirements and a focused test may be enough. Risk reduction must not be confused with paperwork volume.

## 4. Approval boundaries

The agent may inspect and propose. It must not independently perform actions requiring human authority, including destructive data operations, production deployment, paid resource creation, permission changes, secret rotation, external communications, or irreversible migrations. Obtain explicit approval and follow the applicable platform controls.

## 5. Required project records

Maintain only records that provide value. For medium/high complexity, use:
- Project brief and requirements.
- Acceptance criteria.
- Architecture diagram or concise component/data-flow description.
- ADRs for material decisions.
- Data/API contracts.
- Phased implementation plan.
- Risk register.
- Test/verification evidence.
- Release and rollback plan.
- Operational notes/runbook.
