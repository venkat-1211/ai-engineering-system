# Engineering Quality Metrics

## Purpose

Measure engineering outcomes with transparent definitions and known limitations. Metrics support decisions; they do not replace engineering judgment.

## Metric design

For each metric define:
- name and purpose;
- precise formula;
- unit and direction of improvement;
- data source;
- collection method and owner;
- measurement period and baseline;
- target and rationale, if appropriate;
- exclusions and known limitations;
- review cadence.

## Example metric categories

- **Delivery flow:** lead time, cycle time, deployment frequency, work-item aging.
- **Reliability:** service availability, incident rate, mean time to restore, error budget consumption.
- **Quality:** escaped defects, change failure rate, flaky test rate, test execution coverage.
- **Security:** remediation age by severity, overdue findings, dependency update latency.
- **Maintainability:** complexity trends, duplicated code trends, documentation freshness.
- **AI-assisted workflow:** human-rejected suggestions, verified defect rate in AI-generated changes, review rework, tool/action policy violations.

Only use metrics when data is available and definitions are stable. AI-specific metrics must not be used to imply model safety or correctness without an appropriate evaluation design.

## Anti-gaming safeguards

- Do not reward raw output volume or lines of code.
- Avoid using individual metrics as simplistic employee rankings.
- Pair speed metrics with quality and reliability measures.
- Document missing data and changes in collection methods.
- Do not fabricate baselines or targets.
- Review whether a metric creates undesirable incentives.

## Reporting

Show the period, population, source, trend, context, and limitations. Distinguish measured results from estimates and goals.
