# Source Control & Branching

## Requirements
- Use a documented branching model appropriate to team size and release cadence (trunk-based, short-lived feature branches, or controlled release branches).
- Protect the default and production branches. Require review, passing checks, signed/verified commits where policy supports it, and restricted force-push/deletion.
- Keep branches short-lived; avoid long-running divergence. Rebase/merge only according to documented repository policy.
- Require pull requests with purpose, scope, risk, test evidence, migration notes, and rollback notes where relevant.
- Assign code owners to pipeline definitions, deployment scripts, IaC, and security-sensitive configuration.
- Use annotated or signed release tags when supported; tags must map to a reviewed commit and release record.
- Never commit secrets, production data, generated credentials, or environment-specific private configuration.

## Merge controls
Do not merge when required checks are missing, review is absent, conflicts are unresolved, or the change lacks required evidence. Emergency bypasses require a documented human exception and retrospective review.

## Evidence
Record branch protection settings, review approvals, CI result, merge commit, tag, and exception reference if any.
