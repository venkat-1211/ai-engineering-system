# Backup and Restore

## Policy design
Determine what must be protected, including databases, uploaded files, object storage, configuration, encryption keys and infrastructure definitions. Set retention and frequency according to business needs, data loss tolerance, cost and applicable obligations.

## Protection
Use access separation, encryption where appropriate, integrity checks and protection against accidental deletion or ransomware. Keep backup credentials and keys separate from ordinary application credentials. Document exclusions and backup dependencies.

## Restore
Define restoration steps, prerequisites, owners, expected duration and validation checks. Test restoration in a safe environment at a risk-appropriate cadence. Validate application behavior and data consistency, not merely the existence of an archive.

## Evidence
Record backup job outcome, coverage, timestamps, retention, restore-test date, measured restore duration, data-loss point and failures. Redact sensitive values.

## Important
A successful backup job does not prove recoverability. Do not claim backups are valid or restorable without a successful restore test.
