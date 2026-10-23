# Remediation Validation

## What I was checking

This is the follow-up to the [Access Control Review](../03-assessment-and-evidence/access-control-review.md).

The question is simple: **was the extra access removed, and are both users now limited to what their roles allow?**

## Related items

- **Risk:** R-001 Excessive user access
- **Control:** AC-6 Least Privilege
- **Remediation item:** POAM-001
- **Updated evidence:** [Access Retest](access-retest.csv)

## Evidence and decision ownership

| Responsibility | Scenario role | Record supporting this exercise |
|---|---|---|
| Remove excess access and supply updated evidence | IAM Team, the POAM-001 Remediation Owner | `Fix Applied` and `Access After Fix` in [Access Retest](access-retest.csv) |
| Evaluate corrected access and conclude on the retest | Control Assessor | This validation narrative and the comparisons below |
| Coordinate the tracker update | System Security Officer (SSO) | Closed POAM-001 row in the [Remediation Tracker](remediation-tracker.csv) |
| Own the broader R-001 treatment | System Owner | Open R-001 row in the [Risk Register](../02-risk-and-controls/risk-register.csv) |

These are role assignments from the [Responsibility Matrix](../01-context-and-governance/responsibility-matrix.md), not records of separate people performing the work. I authored both the original and retest datasets. The retest is synthetic post-fix evidence; no system change ticket, dated export, execution log, independent assessor sign-off, or closure date is retained. The tracker's target date is a planned deadline, not proof of completion by that date.

## Method

I used the **examine** method from NIST SP 800-53A Rev. 5 and compared the original exceptions with the updated evidence for U-005 and U-009.

The approved role access did not change:

- Finance Analyst: View finance reports
- Support Analyst: Work help desk tickets

No separate exception was documented for the extra ability to edit payroll records or administer servers, so both remained exceptions until that access was removed.

## Retest results

| Account | Original problem | Access after fix | Result |
|---|---|---|---|
| U-005 | Finance Analyst could edit payroll records | View finance reports | Pass |
| U-009 | Support Analyst could administer servers | Work help desk tickets | Pass |

Both accounts now stay within the approved access for their roles.

## Exception-to-closure trace

| Finding / account | Original evidence | Corrective action in POAM-001 | Retest evidence | Scoped disposition |
|---|---|---|---|---|
| A-01 / U-005 | [Original dataset](../03-assessment-and-evidence/access-review.csv): payroll editing exceeds Finance Analyst baseline | Remove payroll editing | [Retest dataset](access-retest.csv): only View finance reports remains | Pass; close A-01 in this exercise |
| A-02 / U-009 | [Original dataset](../03-assessment-and-evidence/access-review.csv): server administration exceeds Support Analyst baseline | Remove server administrator access | [Retest dataset](access-retest.csv): only Work help desk tickets remains | Pass; close A-02 in this exercise |

To reproduce the result, match each account ID across the two CSVs, confirm the approved baseline is unchanged, and compare `Access After Fix` with `Approved Access`. Both must pass before closing their shared POAM-001. This is an examination of recorded permissions, not a live authorization test.

## Decision

**Satisfied for the scoped remediation retest.**

The extra access was removed, the updated evidence matches the approved roles, and both accounts passed the retest. That supports closing POAM-001 within the synthetic exercise. Operational closure would also require retained change and collection records plus documented validation by the assigned assessor.

**POAM-001 status: Closed**

Closure is supported by:

1. U-005 can no longer edit payroll records
2. U-009 no longer has server administrator access
3. approved role access was confirmed and no documented exception supported the extra access
4. updated access evidence was retained
5. both accounts passed the retest

## What remains open

R-001 remains owned by the System Owner, with IAM responsible for the treatment. The next evidence needed is a subsequent dated access review with a reconciled population, independently approved role baseline, and documented disposition of exceptions. The Control Assessor would evaluate that evidence before recommending any broader effectiveness conclusion or residual-risk change. No repeat review, residual-risk score, or system-level risk acceptance is recorded here.

## What this closes

This closes the two exceptions from the original review. It does not prove that every part of AC-6 is working across the entire environment, which is why the broader R-001 risk remains open.
