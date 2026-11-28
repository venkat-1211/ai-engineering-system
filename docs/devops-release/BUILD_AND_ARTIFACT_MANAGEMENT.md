# Build & Artifact Management

- Build from a clean, known source revision and record commit SHA, build ID, toolchain, dependency lockfiles, and build parameters.
- Prefer reproducible builds; document unavoidable nondeterminism.
- Produce immutable, versioned artifacts and calculate cryptographic digests.
- Store artifacts in an access-controlled registry with retention, backup, and audit policies.
- Promote the exact same artifact digest through test, staging, and production.
- Generate provenance/SBOM/signature evidence where supported by the ecosystem and risk.
- Verify artifact integrity and provenance before deployment.
- Restrict artifact overwrite and deletion; separate publish and deploy permissions.
- Do not include credentials, local environment files, test secrets, or unnecessary source/data in release packages.
- Define retention and cleanup without deleting artifacts needed for active releases, investigations, or rollback.

Release record should link source commit → pipeline run → artifact name/version/digest → approvals → deployments.
