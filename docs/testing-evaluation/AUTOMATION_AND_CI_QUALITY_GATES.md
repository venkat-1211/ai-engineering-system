# Test Automation and CI Quality Gates

## Pipeline design
Run fast, high-signal checks early; run broader suites at appropriate merge, scheduled, or release points. Include linting, formatting checks, static analysis, type checks, tests, dependency/security scans, and build validation where relevant.

## Gate design
Define required checks, ownership, failure behavior, rerun policy, and exception authority. A gate should block when a required check fails or cannot produce trustworthy evidence.

## Avoid false greens
Do not mask exit codes, ignore failures broadly, use `|| true` to bypass required checks, or mark skipped jobs as successful. Verify that the intended test suite actually ran and that the pipeline used the expected commit.

## Reproducibility
Pin or constrain tool versions appropriately. Preserve logs and artifacts with access controls and retention suited to sensitivity. Record pipeline run identifiers and commit SHA.

## Human decisions
Automated systems may report evidence and enforce approved rules. They must not grant themselves permission to waive required gates or approve high-impact releases.
