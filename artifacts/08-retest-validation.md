# 08 - AC-6 Remediation Retest and Validation

## What I was checking

This is the follow-up to the access-control assessment in [07-control-assessment.md](07-control-assessment.md).

The question here is simple: **were the two unsupported group memberships actually removed, and do the affected accounts now match their approved roles?**

## Related items

- **Risk:** R-001 Excessive user access
- **Control:** AC-6 Least Privilege
- **Remediation item:** POAM-001
- **Updated evidence:** [08-synthetic-access-retest.csv](08-synthetic-access-retest.csv)

## Method

I used the **examine** method from NIST SP 800-53A Rev. 5 and compared the original exceptions with the updated evidence for U-005 and U-009.

The approved role mappings did not change:

- Finance Analyst → Finance-Read
- Support Analyst → Helpdesk-Users

There was no approval or role-change record supporting the extra Payroll-Write or Server-Admins memberships, so both remained exceptions until they were removed.

## Retest results

| Account | Original problem | Post-remediation access | Result |
|---|---|---|---|
| U-005 | Payroll-Write exceeded the Finance Analyst role | Finance-Read | Pass |
| U-009 | Server-Admins exceeded the Support Analyst role | Helpdesk-Users | Pass |

Both accounts now match the approved role baseline used in the original assessment.

## Decision

**Satisfied for the scoped remediation retest.**

The two exceptions were corrected, the updated evidence matches the approved roles, and both accounts passed the retest. That is enough to close POAM-001.

**POAM-001 status: Closed**

Closure is supported by:

1. Payroll-Write removed from U-005
2. Server-Admins removed from U-009
3. approved role mappings confirmed
4. updated access evidence retained
5. both accounts passing the retest

## What this closes

This closes the two findings from the original assessment. It does not prove that every part of AC-6 is working across the entire environment, which is why the broader R-001 risk remains open.
