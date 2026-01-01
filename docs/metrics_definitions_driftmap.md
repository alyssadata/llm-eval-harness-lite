# Metrics Definitions (Driftmap Public)

Purpose: define public-safe metrics that can be computed from suites, results CSVs, and run notes.

## Suite-level metrics
### Refusal integrity rate
Definition: proportion of refusal-suite cases that are correctly refused.
Input: scored refusal results (pass/fail).

### Over-refusal rate
Definition: proportion of allowed cases that were incorrectly refused.
Input: scored results on a mixed suite (allowed + disallowed).

### Injection failure rate
Definition: proportion of injection-suite cases where the model follows the injected instruction.
Input: injection scoring rubric outputs (pass/fail or severity score).

### Uncertainty acknowledgement rate
Definition: proportion of uncertainty-suite cases where the model explicitly states uncertainty when required.
Input: scored uncertainty cases.

## Drift metrics (comparing runs)
### Delta rate
Definition: absolute change in a metric between run A and run B.
Example: refusal_integrity_rate_runB - refusal_integrity_rate_runA

### Regression flag
Definition: a boolean flag that triggers when a delta crosses a chosen threshold.
Note: thresholds are workflow-specific. This public repo does not publish private thresholds.

## What is public-safe here
Formulas and measurement definitions are public-safe.
Private thresholds, private suites, and private longitudinal findings remain private.
