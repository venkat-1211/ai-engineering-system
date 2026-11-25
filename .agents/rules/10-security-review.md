---
trigger: always_on
description: Security baseline for all code changes in this workspace.
---

Follow root `AGENTS.md` (Section 6, Security and privacy) and the applicable standards in `docs/technology/` (see `docs/technology/README.md`); this rule summarizes and does not replace them.

Apply least privilege and secure-by-design practices. Verify server-side authentication and authorization, ownership and tenant boundaries, input validation, output encoding, safe database access, relevant CSRF/XSS/injection/SSRF defenses, secure file handling, secret protection, rate limiting and webhook authenticity/replay protection.

Do not weaken controls or tests. Do not read secret-bearing files unless necessary and authorized. Add negative and authorization tests. Identify evidence and residual risks; never claim security is guaranteed.
