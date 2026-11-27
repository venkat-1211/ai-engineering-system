# Test Strategy and Risk-Based Verification

## Establish scope
Identify changed components, consumers, dependencies, data flows, interfaces, deployment surfaces, and failure modes. Inspect existing tests and conventions before introducing a new framework.

## Risk assessment
Rate impact and likelihood using project-defined scales. Consider confidentiality, integrity, availability, financial or operational impact, user reach, regulatory applicability (only when established), integration count, novelty, and reversibility. Record assumptions and uncertainty.

## Verification selection
Map each material risk to one or more checks: unit, component, integration, contract, end-to-end, migration, security, accessibility, performance, resilience, backup/restore, or manual exploratory testing. Explain why omitted test levels are not needed.

## Test strategy record
Capture scope, out-of-scope areas, risk items, acceptance criteria, test levels, environments, data, owners, commands, dependencies, exit criteria, and known constraints. Update the strategy when implementation changes materially.

## Proportionality
Do not maximize test count blindly. Prefer the smallest complementary set that gives credible coverage of the important risks. High-impact or hard-to-reverse changes require stronger evidence and appropriate human review.
