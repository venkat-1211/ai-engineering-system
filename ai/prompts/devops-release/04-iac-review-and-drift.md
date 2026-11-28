# Prompt 04 — Infrastructure as Code Review

Perform a review of the supplied IaC changes in read-only mode. Identify providers/modules, version pinning, state backend/locking/backup, resource changes, public exposure, IAM permissions, network boundaries, destructive operations, cost implications, and drift risks.

Do not run apply, destroy, import, state mutation, or commands that alter infrastructure. A plan may be run only in an explicitly authorized safe environment and must not expose sensitive values. Report exact evidence and unresolved questions. Production apply requires human approval.
