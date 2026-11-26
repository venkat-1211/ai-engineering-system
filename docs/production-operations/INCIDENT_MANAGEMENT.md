# Incident Management

## Preparation
Define incident roles, severity criteria, escalation routes, communication channels and service-specific runbooks before incidents occur. Keep contact information in approved access-controlled locations.

## Response lifecycle
1. Detect and validate the signal.
2. Declare an incident when impact or risk warrants it.
3. Assign a human incident lead and technical responders.
4. Establish scope, user impact and a shared timeline.
5. Mitigate safely; preserve evidence.
6. Communicate status at an agreed cadence.
7. Recover and verify user-facing service health.
8. Close the incident and create follow-up actions.

## Severity
Define severity using impact, scope, duration, data/security implications and business criticality. Do not copy generic severity labels without mapping them to the service.

## Safety
Do not run destructive commands, disable security controls, expose data or make production changes without authorization. Prefer reversible mitigations. Escalate suspected compromise through the security response process.

## Records
Capture timestamps, impact, decisions, actions, owners, communications, recovery evidence and unresolved risks. Avoid storing secrets or unnecessary personal data in incident reports.
