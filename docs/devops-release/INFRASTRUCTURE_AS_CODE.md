# Infrastructure as Code

- Version infrastructure definitions with application code or a governed infrastructure repository.
- Review IaC changes as code; require plan/diff review before apply.
- Separate plan and apply permissions. Production apply requires human approval.
- Use remote state with encryption, access control, locking, versioning, and backup.
- Never commit state files, credentials, private keys, or sensitive plan output.
- Pin provider/module versions and review source/provenance.
- Detect and reconcile drift deliberately; do not blindly overwrite emergency/manual changes.
- Test modules and policies in isolated environments.
- Define resource ownership, tagging, cost controls, network boundaries, and deletion protection.
- Destructive changes require impact analysis, backup/recovery validation, and explicit approval.
