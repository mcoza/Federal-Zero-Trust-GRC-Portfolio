# 07A - Modeled Control Assessment

## Purpose

This artifact shows one focused control assessment from evidence to conclusion.

The evidence is synthetic and was created for this portfolio. It does not represent a real organization, real users, or a real federal system.

## Assessment objective

Determine whether modeled user access matches approved role requirements.

## Related risk and control

- **Risk:** R-001 Excessive user access
- **Assessed control:** AC-6 Least Privilege
- **Related remediation item:** POAM-001

AC-2 Account Management is related to the broader account lifecycle, but this exercise does not test the full AC-2 control.

## Assessment method

The assessment uses the **examine** method described in NIST SP 800-53A Rev. 5 terminology.

The modeled population contains 12 accounts, so all 12 records are compared rather than sampling a subset.

## Evidence

- [07-modeled-access-review.csv](07-modeled-access-review.csv)
- approved role-to-group assignments in the `Approved Groups` field
- observed group memberships in the `Observed Groups` field

The evidence file contains the modeled source values only. Pass/fail results and exceptions are documented in this assessment rather than pre-populated in the evidence.

## Expected control condition

Observed group membership should not contain access that is unsupported by the approved role.

## Procedure

1. Read the approved groups for each modeled role.
2. Compare them with the observed groups for each account.
3. Mark the record as a pass when observed access does not exceed approved access.
4. Record an exception when the observed groups contain unsupported access.
5. Trace confirmed exceptions to remediation.

## Results

| Result | Count |
|---|---:|
| Population reviewed | 12 |
| Pass | 10 |
| Exceptions | 2 |

Only two records contain observed groups that are not present in the approved groups.

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

The expected AC-6 condition is not met across the full modeled population because 2 of 12 accounts contain access not supported by the approved role.

In plain language, the least-privilege condition is not operating consistently in this modeled example.

## Remediation

POAM-001 tracks the following actions:

1. Remove Payroll-Write from U-005.
2. Remove Server-Admins from U-009.
3. Review the approved role mappings and access-approval or role-change process related to the two exceptions.
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

## Assessment boundary

This is a focused portfolio exercise, not a complete NIST SP 800-53A assessment. It demonstrates the reasoning pattern of defining an expected condition, examining evidence, identifying exceptions, reaching a finding, and tracing the result into remediation.

Reference: NIST SP 800-53A Rev. 5, Assessing Security and Privacy Controls in Information Systems and Organizations.
