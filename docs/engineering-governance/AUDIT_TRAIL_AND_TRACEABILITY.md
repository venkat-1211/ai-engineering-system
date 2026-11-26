# Audit Trail and Traceability

## Objective

Enable reviewers to reconstruct material decisions and verify what happened, when, by whom, under which authority, and with what evidence.

## Traceability chain

Where relevant, connect:
- requirement or risk;
- design decision;
- implementation change;
- review;
- test or verification result;
- approval;
- release or operational event;
- corrective action.

## Minimum record fields

- stable record ID;
- timestamp and time zone;
- actor or accountable owner;
- action or decision;
- scope and affected artifact;
- rationale;
- approval reference, if required;
- evidence reference;
- outcome and follow-up.

## Integrity and access

Use approved source control, ticketing, CI/CD, logging, and evidence systems. Restrict modification and access according to policy. Preserve provenance and timestamps. Do not expose secrets in logs or reports.

## Limitations

A Git commit proves a repository change was recorded; it does not prove the change was safe, tested, approved, or compliant. A CI result proves only the checks actually run in the stated environment and revision.

## Retention

Follow applicable organizational, contractual, and legal retention rules. Do not invent a universal retention period. Record disposal or archival decisions where required.
