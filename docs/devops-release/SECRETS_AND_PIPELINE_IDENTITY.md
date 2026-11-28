# Secrets & Pipeline Identity

## Secret handling
- Store secrets in an approved secret manager or protected CI/CD secret facility.
- Prefer short-lived credentials, workload identity, federation, or dynamic secrets over long-lived static keys.
- Scope secrets to one environment and one purpose. Rotate and revoke after exposure or suspected compromise.
- Masking is defense-in-depth, not permission to print secrets.
- Never pass secrets in command-line arguments, URLs, source files, prompts, artifacts, or test fixtures.
- Do not echo environment variables or dump process environments in diagnostics.
- Restrict who can read, write, approve, and use production secrets.

## Identity
- Separate CI build identity from CD deployment identity.
- Grant only required actions and resource scopes. Avoid organization-wide administrator credentials.
- Restrict privileged workflows to trusted branches and approved actors.
- Audit identity usage and remove unused credentials promptly.
- Use protected environments and explicit human approvals for production credentials.
