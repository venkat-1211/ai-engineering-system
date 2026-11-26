# Policy Lifecycle and Versioning

## Lifecycle

1. **Draft:** owner prepares purpose, scope, requirements, rationale, and impact.
2. **Review:** relevant technical, security, privacy, legal/compliance, and operational reviewers are consulted as applicable.
3. **Approval:** authorized human approves the policy and effective date.
4. **Publication:** publish the approved version and communicate applicability.
5. **Operation:** teams follow the current approved version and retain evidence where required.
6. **Review:** assess on schedule and after material triggers.
7. **Retirement:** record superseding policy, retirement date, and migration implications.

## Version control

Each policy should have:
- stable identifier;
- title and owner;
- version;
- status;
- approval authority and date;
- effective date;
- next review date;
- change summary;
- superseded version, if any.

Use the repository's normal Git history as supporting change history, not as a substitute for explicit approval records.

## Change principles

- Do not silently change approved policy.
- Policy changes must not silently override higher-priority repository safety, security, or instruction-precedence rules.
- Assess impact on active projects and existing exceptions.
- Communicate material changes.
- Preserve historical versions and decision records according to retention requirements.
- Do not invent approval metadata.
