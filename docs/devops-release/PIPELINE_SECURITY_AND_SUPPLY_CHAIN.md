# Pipeline Security & Software Supply Chain

- Treat pipeline configuration, runners, actions, plugins, base images, package registries, and build dependencies as attack surfaces.
- Pin third-party actions/plugins to immutable versions or commit digests where supported.
- Use trusted registries and verify package integrity/signatures where available.
- Isolate ephemeral runners; do not reuse privileged workspaces for untrusted code.
- Do not expose deployment credentials to untrusted pull requests or fork builds.
- Restrict network egress and runner permissions to required destinations.
- Generate and retain SBOM/provenance/signature data when supported and proportionate to risk.
- Scan source, dependencies, containers, IaC, and secrets with approved tools.
- Define vulnerability severity thresholds, remediation SLAs, and documented exception paths.
- Protect caches and artifacts against tampering and cross-tenant access.
- Apply Stage 10 threat modeling, prompt/tool security, and supply-chain controls to AI-enabled build/release agents.
