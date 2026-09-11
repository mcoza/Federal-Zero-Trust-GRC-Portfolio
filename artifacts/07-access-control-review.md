# 07A - Access Control Review

## What I tested

This is the worked control assessment in the repo.

I used the fictional access data to answer one question: **do these users have only the group memberships their approved roles allow?**

## Related risk and control

- **Risk:** R-001 Excessive user access
- **Assessed control:** AC-6 Least Privilege
- **Remediation item:** POAM-001
- **Retest:** [08-remediation-validation.md](08-remediation-validation.md)

AC-2 Account Management is related to the broader account lifecycle, but this dataset does not test that full process. I kept the assessment tied to AC-6 because that is what the evidence actually supports.

## Method

I used the **examine** method from NIST SP 800-53A Rev. 5.

There are only 12 accounts in the dataset, so I reviewed all 12 instead of taking a sample.

## Evidence

- [07-access-review.csv](07-access-review.csv)
- approved role-to-group assignments in the `Approved Groups` field
- observed memberships in the `Observed Groups` field

The CSV only contains the source data. I kept the pass/fail judgment here so I had to derive the result from the evidence instead of building the answer into the dataset.

## What counts as a pass

Observed group membership should not include access that is unsupported by the approved role.

For each account, I compared the approved groups with the observed groups. If the observed access stayed within the approved role, it passed. If there was extra unsupported access, I recorded an exception.

## Results

| Result | Count |
|---|---:|
| Accounts reviewed | 12 |
| Pass | 10 |
| Exceptions | 2 |

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

## Finding

**Other Than Satisfied for the scoped AC-6 condition.**

Ten accounts matched their approved roles, but two did not. That means least privilege was not being applied consistently across the records I reviewed.

## Remediation

POAM-001 tracks the corrective work for the two exceptions:

1. Remove Payroll-Write from U-005.
2. Remove Server-Admins from U-009.
3. Confirm the approved role baseline for both affected accounts and verify that there is no supporting approval or role-change record for the extra memberships.
4. Retest the corrected accounts.
5. Keep the updated access evidence before closing the item.

The follow-up retest is documented in [08-remediation-validation.md](08-remediation-validation.md).

## Traceability

```text
R-001 Excessive user access
→ AC-6 Least Privilege
→ compare approved vs. observed access
→ 2 exceptions
→ POAM-001
→ access corrected
→ retest
→ POAM-001 closed
```

## What the result means

The finding is limited to the access condition tested here. The successful retest closes these two exceptions; it does not prove that every part of AC-6 is effective across the entire environment.

Reference: NIST SP 800-53A Rev. 5, *Assessing Security and Privacy Controls in Information Systems and Organizations*.
