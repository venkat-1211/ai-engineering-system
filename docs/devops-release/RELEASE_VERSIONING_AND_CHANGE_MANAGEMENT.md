# Release Versioning & Change Management

- Select and document a versioning convention (SemVer or an explicitly defined alternative).
- Ensure release identifiers are unique and traceable to immutable source and artifact digests.
- Maintain a changelog or release notes covering user-visible changes, fixes, known issues, migrations, and operational actions.
- Classify change risk and identify affected services, dependencies, data, security boundaries, and users.
- Require peer review and appropriate test evidence before release approval.
- Production release approval must come from an authorized human role, not an AI agent or automated test.
- Emergency changes require a bounded exception, accountable owner, retrospective review, and evidence.
- Do not silently rewrite published tags or release artifacts.
