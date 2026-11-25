# React Engineering Standard

- Verify React version, rendering framework, router, state tools and build system.
- Build cohesive components with clear props. Keep state close to its owner and avoid duplicating derived state.
- Use effects to synchronize with external systems, not as a default for derived calculations or event logic. Clean up subscriptions and listeners.
- Use stable list keys; do not use array indexes when item identity can change.
- Model loading, empty, success and error states. Treat API responses as untrusted runtime data.
- Prevent stale requests and race conditions with cancellation or request identity.
- Client validation is for usability; server validation and authorization remain mandatory.
- Keep rendering pure. Use memoization only when justified; avoid premature global state.
- Use pagination/virtualization for large collections when appropriate. Check layout shifts and realistic viewport sizes.
- Use semantic HTML, keyboard access, visible focus, labels, accessible names and announced errors. Respect reduced motion and do not rely on color alone.
- Avoid `dangerouslySetInnerHTML` unless content is trusted or correctly sanitized.
- Never expose server secrets in client bundles or public environment variables.
- Test user-visible behavior, keyboard interactions, loading/error/empty states and important permissions.
