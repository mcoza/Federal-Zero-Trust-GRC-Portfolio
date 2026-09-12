# Remediation Validation

## What I was checking

This is the follow-up to the [Access Control Review](../03-assessment-and-evidence/access-control-review.md).

The question is simple: **was the extra access removed, and are both users now limited to what their roles allow?**

## Related items

- **Risk:** R-001 Excessive user access
- **Control:** AC-6 Least Privilege
- **Remediation item:** POAM-001
- **Updated evidence:** [Access Retest](access-retest.csv)

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

## Decision

**Satisfied for the scoped remediation retest.**

The extra access was removed, the updated evidence matches the approved roles, and both accounts passed the retest. That is enough to close POAM-001.

**POAM-001 status: Closed**

Closure is supported by:

1. U-005 can no longer edit payroll records
2. U-009 no longer has server administrator access
3. approved role access was confirmed and no documented exception supported the extra access
4. updated access evidence was retained
5. both accounts passed the retest

## What this closes

This closes the two exceptions from the original review. It does not prove that every part of AC-6 is working across the entire environment, which is why the broader R-001 risk remains open.
