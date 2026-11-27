# Test Quality Review Checklist

- [ ] Test purpose and requirement/risk are clear
- [ ] Assertions verify meaningful observable behavior
- [ ] Negative, boundary, authorization, and failure cases considered
- [ ] Test fails when the intended behavior is broken
- [ ] No tautological assertions or mocks hiding the behavior under test
- [ ] Tests are isolated and do not depend on order
- [ ] Time, network, and concurrency dependencies are controlled
- [ ] Fixtures are safe, minimal, and cleaned up
- [ ] Names and diagnostics make failures understandable
- [ ] No unnecessary duplication or brittle implementation coupling
