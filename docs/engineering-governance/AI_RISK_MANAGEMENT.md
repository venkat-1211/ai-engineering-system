# AI and Engineering Risk Management

## 1. Purpose

Provide a repeatable method to identify, analyze, treat, monitor, and communicate risks arising from software systems and AI-assisted engineering.

## 2. Context before scoring

Record:
- system and intended purpose;
- users and affected stakeholders;
- deployment and operating environment;
- data types and sensitivity;
- external services and dependencies;
- autonomy and human oversight;
- failure consequences and recovery options;
- relevant jurisdictions and organizational policies, if known.

## 3. Risk assessment

For each risk record:
- unique ID and concise scenario;
- asset, process, or stakeholder affected;
- cause, threat, or failure mode;
- potential consequence;
- likelihood and impact with defined scales;
- existing controls and evidence;
- residual risk;
- treatment decision;
- accountable risk owner;
- action owner and due date;
- review trigger and status.

Do not present a numeric score as objective truth. Explain the scale and uncertainty.

## 4. AI-specific considerations

Where AI is used, consider:
- inaccurate or fabricated outputs;
- prompt injection and untrusted content;
- leakage of confidential or personal data;
- insecure generated code or dependencies;
- overbroad tool permissions and unintended actions;
- automation bias and inadequate human oversight;
- model/provider changes and service availability;
- provenance, licensing, and intellectual-property uncertainty;
- evaluation gaps, drift, and monitoring limitations;
- misuse, abuse, and downstream effects.

Applicability depends on the actual AI system and use case. Do not assume every risk applies.

## 5. Risk treatment

Possible treatments:
- avoid the activity;
- reduce likelihood or impact with controls;
- transfer or share risk where appropriate;
- accept residual risk through an authorized human decision.

Record rationale, controls, evidence, owner, approval, and review date. An AI agent cannot accept risk on behalf of an organization.

## 6. Escalation and stop conditions

Stop or escalate when risk exceeds approved tolerance, material facts are unknown, required controls are absent, evidence is insufficient, or the decision requires authority the agent or team does not have.

## 7. Reassessment

Reassess after material changes, incidents, new vulnerabilities, changed data use, new AI capabilities, supplier changes, or relevant regulatory/policy updates.
