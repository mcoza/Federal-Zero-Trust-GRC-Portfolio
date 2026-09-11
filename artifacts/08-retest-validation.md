# 08 - AC-6 Remediation Retest and Validation

## Purpose

This artifact completes the remediation lifecycle for the two access exceptions identified in the R-001 / AC-6 assessment.

The evidence is synthetic and is used only for portfolio demonstration.

## Related items

- **Risk:** R-001 Excessive user access
- **Control:** AC-6 Least Privilege
- **Original assessment:** [07-control-assessment.md](07-control-assessment.md)
- **Remediation item:** POAM-001
- **Updated evidence:** [08-synthetic-access-retest.csv](08-synthetic-access-retest.csv)

## Validation objective

Determine whether the two unsupported group memberships identified in the original assessment were removed and whether the affected accounts now match the approved role requirements.

## Validation method

I used the **examine** method from NIST SP 800-53A Rev. 5.

I compared the original exception records with the updated synthetic access evidence for U-005 and U-009.

## Closure review

The approved role mappings remained unchanged:

- Finance Analyst → Finance-Read
- Support Analyst → Helpdesk-Users

The scenario contained no supporting approval or role-change record for the extra Payroll-Write or Server-Admins memberships. I therefore continued to treat both memberships as unsupported access and validated their removal rather than changing the approved role baseline.

## Retest results

| Account | Original exception | Post-remediation access | Result |
|---|---|---|---|
| U-005 | Payroll-Write exceeded the Finance Analyst role | Finance-Read | Pass |
| U-009 | Server-Admins exceeded the Support Analyst role | Helpdesk-Users | Pass |

Both affected accounts now match the approved role requirements used in the scoped assessment.

## Validation conclusion

**Satisfied for the scoped remediation retest.**

The two exceptions identified in the original AC-6 assessment were corrected in the synthetic evidence. POAM-001 can therefore be closed for this portfolio exercise.

This conclusion is deliberately narrow. It validates remediation of the two identified exceptions; it does not establish that every AC-6 determination or all access controls across the fictional environment are effective.

## Closure decision

POAM-001 status: **Closed**

Closure is supported by:

1. removal of Payroll-Write from U-005
2. removal of Server-Admins from U-009
3. confirmation that the approved role mappings did not change
4. updated synthetic access evidence
5. successful retest of both affected accounts

## Traceability

```text
R-001 Excessive user access
        ↓
AC-6 Least Privilege
        ↓
Initial assessment: Other Than Satisfied
        ↓
2 unsupported group memberships
        ↓
POAM-001
        ↓
Unsupported access removed
        ↓
Updated evidence reviewed
        ↓
2 of 2 retest records pass
        ↓
Scoped remediation validation: Satisfied
        ↓
POAM-001 Closed
```

## Limits

This is a focused synthetic remediation and retest exercise. It demonstrates closure logic for a portfolio finding and does not represent production audit evidence, a complete NIST SP 800-53A assessment, or a determination that the broader environment has no residual access risk.
