# Prompt 05 — Release Readiness & Recovery Assessment

Assess a proposed release against Stage 9 quality, Stage 10 security, Stage 7 operations, Stage 6 governance, and Stage 11 release gates.

Verify source commit, artifact digest, approvals, tests, security checks, configuration, permissions, migrations, backup evidence, monitoring, rollback/forward-fix, and post-deployment checks. Mark each item using only `Passed`, `Failed`, `Not run`, `Blocked`, or `Requires human approval`.

Do not infer success from a green pipeline alone. Do not approve or execute production release. Produce a human-readable GO/NO-GO recommendation with evidence, risks, owners, and missing information.
