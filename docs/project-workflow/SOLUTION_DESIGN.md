# Solution Design and Architecture

## 1. Repository and environment discovery

Before proposing a design, inspect actual evidence:
- Repository structure and entry points.
- Existing architecture and module boundaries.
- Language/framework/runtime versions.
- Dependency manifests and lockfiles.
- Database schema, migrations, and seed data.
- Existing API routes/contracts and integrations.
- Authentication, authorization, and trust boundaries.
- Configuration and secret-management approach.
- Tests, CI, build, deployment, and infrastructure.
- Existing conventions, known limitations, and recent related changes.

Do not assume a framework, version, service, or deployment topology. If evidence is unavailable, record the unknown and ask or propose a clearly marked hypothesis.

## 2. Design concerns

Address applicable concerns:
- Responsibilities and boundaries of components.
- Data ownership and source of truth.
- Request/event/data flows.
- Authentication and authorization enforcement points.
- Validation and trust boundaries.
- Failure modes, retries, idempotency, and timeouts.
- Concurrency and consistency.
- Caching and invalidation.
- Observability and auditability.
- Performance and capacity.
- Deployment, migration, compatibility, and rollback.
- Accessibility and user experience for UI changes.

## 3. Architecture choices

Compare reasonable alternatives using criteria such as:
- Requirement fit.
- Security and privacy.
- Complexity and operational burden.
- Compatibility with existing systems.
- Reliability and performance.
- Cost and team capability.
- Reversibility and vendor lock-in.

Choose the least complex approach that meets requirements. Avoid introducing microservices, queues, caches, abstractions, or dependencies without a concrete need.

## 4. Architecture Decision Records

Create an ADR for material decisions. Include:
- Context and problem.
- Decision drivers and constraints.
- Options considered.
- Decision and rationale.
- Consequences, risks, and trade-offs.
- Status and date.
- Review trigger if the decision may need revisiting.

Do not create ADRs for trivial implementation details.

## 5. Security design

For relevant changes, identify:
- Assets and sensitive data.
- Actors, trust boundaries, and entry points.
- Threats and abuse cases.
- Authentication and authorization requirements.
- Input validation, output encoding, and injection risks.
- Secrets, cryptography, transport, and storage.
- Rate limits and resource exhaustion.
- Logging, audit, and privacy concerns.
- Dependency and supply-chain risks.
- Mitigations and residual risks.

Apply the security baseline and applicable technology-specific standards from the parent AI Engineering System.

## 6. Design review exit criteria

A design is ready when:
- It addresses agreed requirements and acceptance criteria.
- It fits the discovered stack and versions.
- Data and integration impacts are understood.
- Security and failure modes are considered.
- Operational and deployment implications are identified.
- Important trade-offs and assumptions are documented.
- No unresolved high-impact question is being hidden.
