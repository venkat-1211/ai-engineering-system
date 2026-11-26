# Stage 6 — AI Engineering Governance, Compliance & Continuous Improvement

## Purpose

Stage 6 adds a practical governance layer to the AI Engineering System. It defines accountability, risk-based oversight, compliance applicability assessment, evidence traceability, exception handling, quality measurement, and continuous improvement.

This is an **add-on stage**. Merge its directories and files into the existing repository. Do not replace the root `AGENTS.md` with this package or overwrite Stages 1–5.

## Relationship to previous stages

- Stage 1 remains the universal engineering and safety baseline.
- Stage 2 remains the tool-specific instruction and permission guidance.
- Stage 3 remains the technology-specific engineering standards.
- Stage 4 remains the project lifecycle and delivery workflow.
- Stage 5 remains the multi-agent orchestration model.
- Stage 6 governs how these standards are owned, assessed, evidenced, reviewed, and improved.

Where a Stage 6 governance process appears to conflict with a previous-stage safety rule, the safer and more restrictive applicable rule takes precedence. Governance must never weaken security, permissions, human approval, or verification requirements.

## Package contents

- `AGENTS_STAGE_6_ADDENDUM.md` — reference-only integration aid.
- `docs/engineering-governance/` — governance policies and operating guidance.
- `ai/templates/engineering-governance/` — reusable governance records.
- `ai/checklists/engineering-governance/` — review gates.
- `ai/prompts/engineering-governance/` — agent prompts for governance activities.

## Adoption approach

1. Inspect the actual repository, project type, deployment model, data, stakeholders, and applicable jurisdictions.
2. Identify which governance controls are relevant and proportionate.
3. Assign accountable human owners for decisions that require authority.
4. Maintain registers and evidence only where applicable.
5. Review risks, exceptions, quality trends, and improvement actions at an agreed cadence.
6. Record what was not assessed, not applicable, blocked, or not verified.

Do not invent legal obligations, certification status, regulatory applicability, audit evidence, approvals, or quality measurements. A checklist or completed template is not proof of compliance by itself.

## Safe integration

- Review every file before adopting it.
- Merge only the Stage 6 directories and files.
- Do not overwrite root `AGENTS.md`.
- Do not automatically enable new permissions or integrations.
- Integrate selected guidance into root `AGENTS.md` only through a separately reviewed change.
- Keep `AGENTS_STAGE_6_ADDENDUM.md` as a reference-only aid, not a second active root instruction file.

## Suggested validation

After merging, perform a read-only audit that checks file completeness, cross-references, consistency with Stages 1–5, governance safety rules, and Git change scope. Do not commit until the audit passes and the user has reviewed the staged file list.
