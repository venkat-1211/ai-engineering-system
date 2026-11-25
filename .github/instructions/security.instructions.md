---
applyTo: "**/*"
---

# Security-focused guidance

Follow root `AGENTS.md` and `docs/AI_ENGINEERING_STANDARD.md`.

For relevant changes, verify server-side authorization, object ownership and tenant isolation; input validation; context-appropriate output encoding; safe database access; CSRF/XSS/injection/SSRF defenses; safe file uploads; secret protection; rate limits; webhook authenticity and replay protection.

Do not claim security merely because a checklist was followed. Report threat scenarios, controls, test evidence and residual risks.
