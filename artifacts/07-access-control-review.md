# 07A - Access Control Review

## What I tested

I reviewed 12 fictional user accounts to answer one question: **can these users do anything their approved roles do not allow?**

## Related risk and control

- **Risk:** R-001 Excessive user access
- **Assessed control:** AC-6 Least Privilege
- **Workpaper:** [07B-access-review-workpaper.md](07B-access-review-workpaper.md)
- **Remediation item:** POAM-001
- **Retest:** [08-remediation-validation.md](08-remediation-validation.md)

AC-2 Account Management is related to the broader account lifecycle, but this dataset does not test that full process. I kept the assessment tied to AC-6 because that is what the evidence supports.

## Method

I used the **examine** method from NIST SP 800-53A Rev. 5.

There are only 12 accounts in the dataset, so I reviewed all 12 instead of taking a sample. The population, criteria, procedure, and account-level testing are documented in the [Access Review Workpaper](07B-access-review-workpaper.md).

## Evidence

- [07-access-review.csv](07-access-review.csv)
- approved access in the `Approved Access` field
- actual access in the `Observed Access` field

The `Approved Access` field is the authorization baseline for this scenario. No separate exception is documented for U-005 or U-009.

## What counts as a pass

A user passes when the observed access stays within the approved access for the role.

If the user can do something outside that approved access and there is no documented exception, I record an exception.

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
3. Confirm the approved role baseline for both accounts and confirm that no documented exception supports the extra access.
4. Retest the corrected accounts.
5. Keep the updated access evidence before closing the item.

The follow-up retest is documented in [08-remediation-validation.md](08-remediation-validation.md).

## Traceability

```text
R-001 Excessive user access
→ AC-6 Least Privilege
→ WP-AC6-001
→ compare approved access with actual access
→ 2 exceptions
→ POAM-001
→ access corrected
→ retest
→ POAM-001 closed
```

## What the result means

The finding is limited to the access condition tested here. The successful retest closes these two exceptions. It does not prove that every part of AC-6 is effective across the entire environment.

Reference: NIST SP 800-53A Rev. 5, *Assessing Security and Privacy Controls in Information Systems and Organizations*.
