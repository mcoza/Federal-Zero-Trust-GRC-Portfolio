# 07A - Access Control Review

## What I tested

I reviewed 12 fictional user accounts to answer one question: **can these users do anything their approved roles do not allow?**

## Related risk and control

- **Risk:** R-001 Excessive user access
- **Assessed control:** AC-6 Least Privilege
- **Remediation item:** POAM-001
- **Retest:** [08-remediation-validation.md](08-remediation-validation.md)

AC-2 Account Management is related to the broader account lifecycle, but this dataset does not test that full process. I kept the assessment tied to AC-6 because that is what the evidence supports.

## Method

I used the **examine** method from NIST SP 800-53A Rev. 5.

There are only 12 accounts in the dataset, so I reviewed all 12 instead of taking a sample.

## Evidence

- [07-access-review.csv](07-access-review.csv)
- approved access in the `Approved Access` field
- actual access in the `Observed Access` field
- approval or role-change records when observed access falls outside the approved role

The CSV contains the account and access data. For the two accounts with extra access, I also checked whether any approval or role-change record supported it. None did.

## What counts as a pass

A user passes when the observed access is supported by the approved role or another documented approval.

If the user can do something outside that approved access and there is no supporting approval, I record an exception.

## Results

| Result | Count |
|---|---:|
| Accounts reviewed | 12 |
| Pass | 10 |
| Exceptions | 2 |

### Exception A-01

- **Account:** U-005
- **Role:** Finance Analyst
- **Approved access:** View finance reports
- **Extra access found:** Edit payroll records

### Exception A-02

- **Account:** U-009
- **Role:** Support Analyst
- **Approved access:** Work help desk tickets
- **Extra access found:** Administer servers

## Finding

**Other Than Satisfied for the scoped AC-6 condition.**

Ten accounts stayed within their approved access, but two did not. Least privilege was not being applied consistently across the records I reviewed.

## Remediation

POAM-001 tracks the corrective work for the two exceptions:

1. Remove the ability to edit payroll records from U-005.
2. Remove server administrator access from U-009.
3. Confirm the approved role baseline for both accounts and verify that there is no approval or role-change record supporting the extra access.
4. Retest the corrected accounts.
5. Keep the updated access evidence before closing the item.

The follow-up retest is documented in [08-remediation-validation.md](08-remediation-validation.md).

## Traceability

```text
R-001 Excessive user access
→ AC-6 Least Privilege
→ compare approved access with actual access
→ check support for any extra access
→ 2 exceptions
→ POAM-001
→ access corrected
→ retest
→ POAM-001 closed
```

## What the result means

The finding is limited to the access condition tested here. The successful retest closes these two exceptions. It does not prove that every part of AC-6 is effective across the entire environment.

Reference: NIST SP 800-53A Rev. 5, *Assessing Security and Privacy Controls in Information Systems and Organizations*.
