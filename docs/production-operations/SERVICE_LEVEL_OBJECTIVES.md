# Service Level Objectives

## Terms
- SLI: a measured indicator of service behavior.
- SLO: a target for an SLI over a defined window.
- SLA: an external or contractual commitment, if one exists.
- Error budget: the permitted unreliability implied by an SLO.

## Design
Choose indicators that reflect user experience, such as successful request ratio, latency distribution, job completion, data freshness or availability. Define numerator, denominator, exclusions, measurement source, window and owner.

Targets must be agreed with accountable stakeholders and supported by baseline evidence. Do not invent targets or describe an internal SLO as a contractual SLA.

## Error budgets
If adopted, define how the budget is calculated, reviewed and used to guide release risk. Budget policy must identify the human decision-maker and exception path.

## Small projects
A lightweight health objective or explicit absence of a formal SLO may be appropriate. Record the reason and operational expectations.

## Review
Reassess indicators when architecture, usage, business impact or dependencies change. Report measurement gaps and uncertainty.
