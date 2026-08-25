# 07A - Control Assessment

## Purpose

This example shows how I went from the access data to an assessment result.

The evidence is synthetic. It does not represent a real organization, real users, or a real federal system.

## Assessment objective

Determine whether user access matches approved role requirements.

## Related risk and control

- **Risk:** R-001 Excessive user access
- **Assessed control:** AC-6 Least Privilege
- **Related remediation item:** POAM-001

AC-2 Account Management is related to the broader account lifecycle, but this exercise does not test the full AC-2 control.

## Assessment method

I used the **examine** method from NIST SP 800-53A Rev. 5.

The dataset only has 12 accounts, so I reviewed all 12 instead of taking a sample.

## Evidence

- [07-modeled-access-review.csv](07-modeled-access-review.csv)
- approved role-to-group assignments in the `Approved Groups` field
- observed group memberships in the `Observed Groups` field

The CSV only contains the source data. I kept the pass/fail results in this assessment so the answer is not already built into the evidence.

## Expected control condition

Observed group membership should not contain access that is unsupported by the approved role.

## Procedure

1. Read the approved groups for each role.
2. Compare them with the observed groups for each account.
3. Mark the record as a pass when observed access does not exceed approved access.
4. Record an exception when the observed groups contain unsupported access.
5. Trace confirmed exceptions to remediation.

## Results

| Result | Count |
|---|---:|
| Accounts reviewed | 12 |
| Pass | 10 |
| Exceptions | 2 |

Only two records contain observed groups that are not in the approved groups.

### Exception A-01

- **Account:** U-005
- **Role:** Finance Analyst
- **Approved access:** Finance-Read
- **Observed access:** Finance-Read; Payroll-Write
- **Unsupported access:** Payroll-Write

### Exception A-02

- **Account:** U-009
- **Role:** Support Analyst
- **Approved access:** Helpdesk-Users
- **Observed access:** Helpdesk-Users; Server-Admins
- **Unsupported access:** Server-Admins

## Assessment finding

**Other Than Satisfied**

The AC-6 condition is not met across all 12 accounts because two contain access that is not supported by the approved role.

Put simply, least privilege is not being applied consistently in this example.

## Remediation

POAM-001 tracks these actions:

1. Remove Payroll-Write from U-005.
2. Remove Server-Admins from U-009.
3. Review the approved role mappings and the access approval or role change process related to the two exceptions.
4. Retest the corrected accounts after remediation.
5. Retain updated access evidence before closing the item.

## Traceability

```text
R-001 Excessive user access
        ↓
AC-6 Least Privilege
        ↓
Expected condition: access matches approved role
        ↓
Compare approved vs observed access
        ↓
2 exceptions found
        ↓
Assessment finding: Other Than Satisfied
        ↓
POAM-001
        ↓
Correct access + retain evidence + retest before closure
```

## Limits of this example

This is a focused portfolio exercise, not a complete NIST SP 800-53A assessment. It shows the basic process of setting a condition, reviewing evidence, identifying exceptions, reaching a finding, and tracing that finding into remediation.

Reference: NIST SP 800-53A Rev. 5, Assessing Security and Privacy Controls in Information Systems and Organizations.