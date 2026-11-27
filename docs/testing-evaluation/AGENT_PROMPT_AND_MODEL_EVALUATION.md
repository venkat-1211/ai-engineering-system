# Agent, Prompt and Model Evaluation

## Define the task
Specify intended capability, allowed tools, prohibited actions, expected output, evaluation context, and failure consequences. Keep evaluation tasks representative of actual work.

## Build an evaluation set
Use versioned cases covering common, boundary, ambiguous, adversarial, and failure scenarios. Use synthetic or authorized data. Avoid leaking answer keys or sensitive production content into prompts or logs.

## Score observable outcomes
Evaluate correctness, completeness, instruction adherence, evidence quality, safe tool use, reproducibility, and appropriate uncertainty. Use explicit rubrics and record evaluator method. Human review is required where automated scoring is unreliable or consequences are high.

## Compare changes fairly
Record model/version, prompt/template version, tool configuration, sampling settings where applicable, dataset version, and run date. Change one factor at a time where practical. Re-run regression cases after prompt, model, or tool changes.

## Limits
A benchmark score is not a guarantee of real-world reliability. Do not claim statistical significance from small or biased samples. Protect evaluation data and disclose limitations.
