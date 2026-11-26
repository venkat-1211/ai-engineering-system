# Change Management and Maintenance

## 1. Change classification

Classify incoming work as appropriate:
- New capability.
- Enhancement.
- Defect correction.
- Refactor or technical-debt reduction.
- Security update.
- Dependency/runtime upgrade.
- Data/schema migration.
- Infrastructure/operational change.
- Incident or emergency change.

Classification informs risk and review depth; it does not replace requirements or verification.

## 2. Change impact assessment

Identify affected users, modules, data, APIs, integrations, permissions, infrastructure, costs, documentation, and operational procedures. Check backward compatibility and existing consumers.

For urgent fixes, keep scope narrow, preserve evidence, and complete follow-up review/documentation after stabilization.

## 3. Technical debt

Record debt with:
- Description and location.
- User, security, reliability, or delivery impact.
- Likelihood and consequence.
- Suggested remediation.
- Priority and owner, if known.

Do not hide known security or reliability risks as ordinary low-priority cleanup.

## 4. Incident learning

After a significant incident:
- Restore service safely first.
- Preserve relevant logs/evidence while protecting sensitive data.
- Establish timeline and customer impact.
- Identify contributing factors without blame.
- Record corrective and preventive actions.
- Add monitoring/tests/runbook updates.
- Track owners and completion.

## 5. Documentation lifecycle

Keep architecture, setup, API contracts, data model, runbooks, and decision records aligned with the actual system. Remove obsolete instructions only after checking whether they are still referenced. Avoid documenting secrets or sensitive operational details in public repositories.
