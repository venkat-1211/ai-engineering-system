# Engineering Governance

## Objective

Provide a risk-based operating model for governing engineering work and AI-assisted development. Governance should make decisions accountable and evidence-based without creating unnecessary bureaucracy.

## Core principles

1. **Accountability:** Every material decision has an identifiable accountable owner.
2. **Proportionality:** Control depth reflects impact, risk, data sensitivity, and operational exposure.
3. **Evidence:** Claims are supported by dated, attributable evidence.
4. **Transparency:** Unknown, unassessed, blocked, and not-applicable states are explicit.
5. **Human authority:** AI agents may analyze and recommend; they do not acquire organizational authority.
6. **Lifecycle:** Controls are reviewed when systems, risks, laws, dependencies, or operating conditions change.
7. **Continuous improvement:** Findings lead to owned actions and follow-up verification.

## Operating cycle

1. Establish project context and accountable owners.
2. Identify stakeholders, assets, data, intended use, and impact.
3. Assess risks and determine applicable obligations.
4. Select controls and define evidence.
5. Monitor quality, risks, exceptions, and changes.
6. Review outcomes and approve corrective actions.
7. Reassess after material changes and on the agreed cadence.

## Status vocabulary

Use explicit states. Recommended governance record statuses:
- `Draft`
- `Under review`
- `Approved`
- `Rejected`
- `Active`
- `Expired`
- `Closed`
- `Not applicable`
- `Not assessed`
- `Blocked`

Do not use `Approved` to mean merely drafted, discussed, or suggested. Record who approved and when.

## Relationship to other stages

Stage 6 governs accountability and evidence for controls established in Stages 1–5. It does not duplicate their technical instructions or replace project-specific engineering judgment.
