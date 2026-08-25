# 07A - Modeled Control Assessment

## Purpose

This artifact shows one small control assessment from evidence to conclusion.

The evidence is synthetic and was created for this portfolio. It does not represent a real organization, real users, or a real federal system.

## Assessment objective

Determine whether modeled user access is consistent with approved role requirements.

## Related risk and controls

- **Risk:** R-001 Excessive user access
- **Controls:** AC-2 Account Management and AC-6 Least Privilege
- **Related remediation item:** POAM-001

## Assessment method

The assessment uses the **examine** method described in NIST SP 800-53A Rev. 5 terminology.

Because the modeled population is small, I reviewed all 12 records instead of sampling a subset.

## Evidence

- [07-modeled-access-review.csv](07-modeled-access-review.csv)
- modeled approved role-to-group assignments
- modeled observed group memberships

## Test criteria

A record passes when the observed group memberships match the groups approved for the user's modeled role.

A record is an exception when the observed access contains a group that is not supported by the approved role.

## Procedure

1. Identify the approved groups for each modeled role.
2. Compare the approved groups with the observed group memberships for each account.
3. Mark the account as Pass when observed access matches the approved role.
4. Mark the account as Exception when unsupported access is present.
5. Document the unsupported group and trace the finding to remediation.

## Results

| Result | Count |
|---|---:|
| Population reviewed | 12 |
| Pass | 10 |
| Exceptions | 2 |

### Exception A-01

- **Account:** U-005
- **Role:** Finance Analyst
- **Approved access:** Finance-Read
- **Observed additional access:** Payroll-Write
- **Finding:** Payroll-Write is not supported by the approved role.

### Exception A-02

- **Account:** U-009
- **Role:** Support Analyst
- **Approved access:** Helpdesk-Users
- **Observed additional access:** Server-Admins
- **Finding:** Server-Admins is not supported by the approved role and introduces unnecessary administrative access.

## Conclusion

The modeled control objective is **partially met but not operating consistently** across the reviewed population.

Ten accounts matched the approved access expectation, but two exceptions show that unsupported access can remain assigned. That supports a finding against the modeled access-review and least-privilege process rather than a conclusion that the control is fully effective.

## Remediation

POAM-001 tracks the following actions:

1. Remove Payroll-Write from U-005.
2. Remove Server-Admins from U-009.
3. Review the role mapping and provisioning / role-change process that allowed the unsupported access.
4. Retest the affected accounts after remediation.
5. Retain updated access-review evidence before closing the item.

## Traceability

```text
R-001 Excessive user access
        ↓
AC-2 / AC-6
        ↓
Expected condition: access matches approved role
        ↓
Modeled evidence reviewed
        ↓
2 exceptions found
        ↓
Control conclusion: not operating consistently
        ↓
POAM-001
        ↓
Remediation + retest before closure
```

## Assessment boundary

This is a focused portfolio example, not a complete NIST SP 800-53A assessment. It demonstrates the reasoning pattern of defining criteria, examining evidence, documenting exceptions, reaching a conclusion, and tracing the result into remediation.

Reference: NIST SP 800-53A Rev. 5, Assessing Security and Privacy Controls in Information Systems and Organizations.
