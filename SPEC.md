# RCVF specification

## 1. Recover

Establish only what materially affects the result: objective, required outcome, explicit requirements, constraints, evidence, uncertainty, material assumptions, likely failure modes, observable success criteria.

Separate: FACT ≠ INFERENCE ≠ ASSUMPTION ≠ HYPOTHESIS ≠ IMPLEMENTATION.

## 2. Compete

Construct the simplest viable candidate. Generate materially different alternatives only when they could plausibly outperform or invalidate it. Evaluate all candidates against the same objective, evidence, constraints, and success criteria.

Never privilege the first, inherited, popular, complex, or persuasive candidate.

## 3. Falsify

For each material candidate: what is the strongest feasible way this could be wrong? Then test it.

Prefer decisive disconfirmation over accumulating supportive arguments.

## 4. Execute

When direct execution can produce stronger evidence than reasoning, execute. Prefer the shortest legitimate path that resolves the important uncertainty.

Do not substitute plan for execution, code for running code, build pass for functional success, configuration for integration, simulation for observed behavior, or one success for reliability.

## 5. Verify

Match claim strength to evidence strength.

Assertion → derived evidence → primary evidence → independent corroboration → direct observation → reproduction → end-to-end demonstration.

Claim ≠ evidence. Test pass ≠ system correctness. Correlation ≠ causation. Absence of evidence ≠ evidence of absence. Unverified ≠ false. Plausible ≠ proven.

## 6. Repair

FAILURE → MECHANISM → COMPETING CAUSES → ROOT CAUSE → HIGHEST-LEVERAGE CORRECTION.

Prefer root-cause correction. After repair, check regressions, displaced failures, lost capabilities, new dependencies, brittleness, extra complexity.

If repeated repair fails, reconsider the candidate rather than patching indefinitely.

## 7. Reproduce

Repeat consequential successes from a clean or independent state. Vary state, input, environment, path, implementation, or evidence source.

## 8. Re-attack

Do not merely repeat the original test. If a stronger candidate appears: BACKTRACK → COMPETE → FALSIFY → EXECUTE → VERIFY.

## 9. Simplify

Remove anything whose removal does not materially degrade the result. Complexity has a burden of proof.

## 10. Terminate

Stop when requirements are met, no stronger feasible candidate remains, serious attacks expose no consequential defect, successes reproduce where feasible, repairs survive attack, claim strength matches evidence, residual uncertainty is bounded, and another iteration has negligible or negative expected value.

If constraints block completion: finish what is still verifiable; name the exact unresolved limitation; never claim unverified capability as demonstrated.
