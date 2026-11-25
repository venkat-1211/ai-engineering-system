# Universal Application Security Baseline

This is a review aid, not a guarantee of security. Adapt it to the application's threat model, data sensitivity and deployment environment.

## Authentication and sessions
- [ ] Protected routes require authentication.
- [ ] Passwords use an approved password-hashing mechanism.
- [ ] Session/token lifecycle, expiry, rotation and revocation are considered.
- [ ] Cookie flags and transport protections are configured appropriately.
- [ ] Authentication errors do not reveal unnecessary account information.

## Authorization
- [ ] Every sensitive server-side operation checks permission.
- [ ] Object-level access and ownership are verified.
- [ ] Tenant boundaries are enforced on reads and writes.
- [ ] Privileged actions require appropriate roles/permissions.
- [ ] UI visibility is not treated as authorization.

## Input and output
- [ ] Inputs are validated at trust boundaries.
- [ ] Database access uses parameterized queries or safe ORM mechanisms.
- [ ] Output is encoded for its rendering context.
- [ ] File uploads enforce type, size, storage and access controls.
- [ ] Redirects, URL fetches and external input are checked for relevant abuse cases.

## Web and API protections
- [ ] CSRF protection is applied where relevant.
- [ ] CORS is restricted to intended origins.
- [ ] Rate limits and abuse controls protect sensitive operations.
- [ ] Errors do not expose stack traces or internal secrets in production.
- [ ] Webhooks validate authenticity and defend against replay where applicable.

## Data and secrets
- [ ] Secrets are not committed to source control.
- [ ] Sensitive values are not logged or exposed in URLs.
- [ ] Data collection and retention are minimized.
- [ ] Encryption is used where required by the threat model and policy.
- [ ] Backups and exports have appropriate access controls.

## Dependencies and operations
- [ ] Dependencies are maintained and vulnerability-audited.
- [ ] Debug/development settings are disabled in production.
- [ ] Database and service credentials follow least privilege.
- [ ] Destructive operations have approval and recovery plans.
- [ ] Security-relevant events are logged without leaking sensitive data.

## Evidence
For each applicable control, record the code/configuration location and test or review evidence. Mark unknown items as needing investigation rather than assuming they are safe.
