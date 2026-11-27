# Test Levels and Complementary Coverage

## Unit tests
Verify small units and decision logic quickly with isolated dependencies. They do not prove integration wiring or real infrastructure behavior.

## Component and integration tests
Verify boundaries between modules, persistence, queues, caches, external adapters, and configuration. Use realistic dependencies selectively and control their lifecycle.

## Contract tests
Verify agreed request/response, event, schema, and compatibility expectations between independently deployed components. Version contracts and test backward/forward compatibility where required.

## End-to-end tests
Cover a small number of critical user journeys through deployed-like paths. Keep them focused; broad E2E suites can be slow and brittle.

## Manual and exploratory testing
Use for usability, unusual workflows, visual inspection, and areas with weak automation. Record scope, environment, steps, observations, and evidence.

## Balance
The familiar test pyramid is a heuristic, not a law. Choose a distribution that reflects architecture and risk. No single level substitutes for all others.
