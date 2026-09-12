# Access Review Workpaper

## Workpaper purpose

This workpaper documents how I tested the scoped R-001 access condition behind the [Access Control Review](access-control-review.md).

| Field | Value |
|---|---|
| Workpaper ID | WP-AC6-001 |
| Risk | R-001 Excessive user access |
| Control | AC-6 Least Privilege |
| Assessment role in scenario | Control Assessor |
| Assessment method | Examine |
| Population | 12 user accounts |
| Accounts tested | 12 |
| Coverage | 100% of the available population |
| Result | Other Than Satisfied for the scoped AC-6 condition |
| Remediation item | POAM-001 |

## Objective

Determine whether the users in the review population have access beyond what their approved roles allow.

## Scope and criteria

The review compares two fields in the access dataset:

- `Approved Access`: the authorization baseline for the role in this scenario
- `Observed Access`: the access the account actually has

An account passes when observed access stays within the approved access. An account is recorded as an exception when observed access includes an additional capability and no documented exception supports it.

This workpaper evaluates that specific least-privilege condition. It does not extend the conclusion to the full account lifecycle or other controls that would require different evidence.

## Evidence used

| Evidence | Use in the test |
|---|---|
| [Access Review Data](access-review.csv) | Population and account-level approved versus observed access |
| `Approved Access` field | Role authorization baseline for the scenario |
| `Observed Access` field | Actual access compared with the approved baseline |

No separate exception is documented for U-005 or U-009 in the scenario evidence.

## Population and sampling decision

The available population contains 12 accounts. Because the population is small, I tested all 12 instead of selecting a sample.

```text
Population: 12
Sample:     12
Coverage:   100%
```

This removes sampling uncertainty for the dataset being reviewed. It does not make the result representative of users outside that dataset.

## Test procedure

1. Confirm the population in `access-review.csv` contains 12 accounts.
2. For each account, identify the role and approved access.
3. Compare `Observed Access` with `Approved Access`.
4. Record a pass when observed access stays within the approved baseline.
5. Record an exception when observed access contains an additional capability without documented support.
6. Summarize the result and send confirmed exceptions into remediation.

## Account-level testing

| Account | Role | Approved access | Observed access | Result |
|---|---|---|---|---|
| U-001 | Finance Analyst | View finance reports | View finance reports | Pass |
| U-002 | HR Analyst | View employee records | View employee records | Pass |
| U-003 | Operations Analyst | View operations reports | View operations reports | Pass |
| U-004 | Support Analyst | Work help desk tickets | Work help desk tickets | Pass |
| U-005 | Finance Analyst | View finance reports | View finance reports; Edit payroll records | Exception A-01 |
| U-006 | Application Analyst | Use business applications | Use business applications | Pass |
| U-007 | Network Analyst | Review network configurations | Review network configurations | Pass |
| U-008 | Security Analyst | Review security alerts; Investigate SIEM events | Review security alerts; Investigate SIEM events | Pass |
| U-009 | Support Analyst | Work help desk tickets | Work help desk tickets; Administer servers | Exception A-02 |
| U-010 | Backup Operator | Run backups; Restore data | Run backups; Restore data | Pass |
| U-011 | Remote Support | Work help desk tickets; Connect to systems remotely | Work help desk tickets; Connect to systems remotely | Pass |
| U-012 | Application Analyst | Use business applications | Use business applications | Pass |

## Exception detail

### A-01: U-005

The Finance Analyst role is approved to view finance reports. The observed access also allows the account to edit payroll records.

**Assessment result:** Exception

### A-02: U-009

The Support Analyst role is approved to work help desk tickets. The observed access also allows the account to administer servers.

**Assessment result:** Exception

## Workpaper conclusion

| Result | Count |
|---|---:|
| Accounts tested | 12 |
| Pass | 10 |
| Exceptions | 2 |

**Assessment conclusion: Other Than Satisfied for the scoped AC-6 condition.**

The two exceptions are sufficient to show that least privilege was not applied consistently across this review population.

## Remediation and retest trace

```text
WP-AC6-001
→ A-01 and A-02
→ POAM-001
→ access removed
→ ../04-remediation-and-validation/access-retest.csv
→ scoped retest Satisfied
→ POAM-001 Closed
```

The remediation result is documented in [Remediation Validation](../04-remediation-and-validation/remediation-validation.md). The successful retest closes the two exceptions, while the broader R-001 risk remains open pending enough evidence to judge the wider access-review process.

Reference: NIST SP 800-53A Rev. 5, *Assessing Security and Privacy Controls in Information Systems and Organizations*.
