# Production Operating Model

## Objectives
Define how a service is owned, operated, changed, supported and retired after release.

## Service record
For each production service record: service name and purpose; business and technical owners; critical dependencies; data classification; environments; deployment method; support hours; escalation contacts; monitoring locations; backup and recovery approach; and known operational limitations.

## Environment separation
Keep development, test, staging and production appropriately separated. Production data must not be copied into lower environments unless explicitly authorized and protected through approved minimization or anonymization. Use environment-specific configuration and access controls.

## Ownership
Assign a human service owner and operational contact. AI agents may prepare analysis and proposed changes but cannot accept operational risk, approve production changes or assume incident command.

## Operational lifecycle
1. Prepare operational design before release.
2. Verify dashboards, alerts, runbooks, access and recovery evidence.
3. Release through approved change controls.
4. Monitor service health and user impact.
5. Manage incidents and recurring problems.
6. Review capacity, dependencies and operational risks.
7. Plan supported retirement, data disposition and credential revocation.

## Minimum evidence
Maintain a service record, operational readiness decision, change history, incident records where applicable, backup/restore evidence where applicable, and review actions.
