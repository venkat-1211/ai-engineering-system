# JavaScript and TypeScript Engineering Standard

- Verify runtime, compiler, package manager and module system from repository evidence.
- Prefer TypeScript for new or substantially changed code when the project supports it; do not migrate the whole project without approval.
- Avoid `any`; use `unknown` at untrusted boundaries and narrow it. TypeScript types do not perform runtime validation.
- Respect strict compiler settings where compatible. Avoid unsafe assertions used only to silence errors.
- Follow the existing ESM/CommonJS convention and avoid circular dependencies.
- Keep modules cohesive and separate domain logic from UI, transport and infrastructure where useful.
- Handle promise rejections; avoid floating promises, unbounded concurrency and blocking event-loop work.
- Use timeouts/cancellation for long-running network work where appropriate.
- Do not swallow exceptions or return success-shaped fallbacks after failures.
- Treat URL parameters, browser storage, API responses, messages and user input as untrusted.
- Avoid `eval`, `Function` and unsafe dynamic code. Prevent XSS and prototype-pollution risks.
- Keep secrets on trusted server-side components; never embed them in client bundles.
- Use the repository's package manager and lockfile consistently. Review dependency ownership, maintenance, license and security.
- Use configured lint, format, type-check and test tools.
