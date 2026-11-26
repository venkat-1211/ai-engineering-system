# Requirements Engineering

## 1. Start with the problem

Clarify:
- Who experiences the problem?
- What are they trying to accomplish?
- What currently happens?
- What is painful, risky, slow, expensive, or impossible?
- Why is a change needed now?
- What outcome would demonstrate success?

Do not jump directly from a requested implementation (“add a button”, “use Redis”, “rewrite this page”) to coding. Confirm the underlying need while respecting explicit constraints.

## 2. Requirement categories

### Functional
Describe observable system behavior: actors, preconditions, actions, business rules, outputs, state changes, and failure behavior.

### Non-functional
Specify measurable or reviewable quality attributes as relevant:
- Security and privacy.
- Performance and capacity.
- Availability and recovery.
- Accessibility and usability.
- Browser/device/platform compatibility.
- Scalability and maintainability.
- Logging, monitoring, and supportability.
- Data retention, auditability, and compliance.

### Constraints and dependencies
Record required technologies, supported versions, hosting limitations, deadlines, integrations, budgets, contracts, and organizational policies. Distinguish hard constraints from preferences.

## 3. Scope discipline

Explicitly list:
- In scope.
- Out of scope.
- Deferred/future work.
- Existing behavior that must remain unchanged.

Do not add features, dependencies, refactors, or UI redesigns that are not required or approved. If a necessary technical change expands scope, explain why and request approval.

## 4. Acceptance criteria

Use clear, testable statements. Prefer Given/When/Then where it helps.

Example:
- Given an authenticated user with permission `invoice.view`, when the user opens an invoice they are authorized to access, then the invoice details are displayed.
- Given an authenticated user without that permission, when they request the same resource directly through the API, then access is denied and no protected data is returned.
- Given invalid input, when the request is submitted, then validation errors are returned without persisting invalid data.

Acceptance criteria should cover happy paths, validation, permissions, error states, boundaries, and relevant accessibility/responsive behavior.

## 5. Questions and ambiguity

Ask a focused question when an unresolved detail could change:
- User-visible behavior or business rules.
- Data shape, migration, or retention.
- Authentication, authorization, or privacy.
- API compatibility or integrations.
- Architecture, cost, performance, or deployment.
- Acceptance criteria or delivery scope.

For low-impact uncertainty, make a conservative assumption, label it, and avoid irreversible decisions. Never present an assumption as a confirmed requirement.

## 6. Requirement quality review

A requirement is ready when it is:
- Necessary and in scope.
- Clear and unambiguous.
- Feasible with known constraints.
- Testable or otherwise verifiable.
- Consistent with other requirements.
- Assigned an owner or source.
- Traceable to acceptance criteria and planned verification.
