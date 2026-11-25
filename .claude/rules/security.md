---
paths:
  - "**/*"
---

Follow root `AGENTS.md` and `docs/AI_ENGINEERING_STANDARD.md`.

For security-sensitive changes, trace trust boundaries; verify server-side and object-level authorization; consider tenant isolation, injection, XSS, CSRF, SSRF, file handling, secrets, webhook spoofing/replay and abuse controls. Add negative and authorization tests. Report threat, control, evidence and residual risk. Do not read secret-bearing files unless necessary and authorized.
