# 04A - POA&M Method

## Purpose

This tracker documents weaknesses or findings, related risks, mapped controls, remediation plans, action owners, target dates, status, and closure evidence.

The goal is to show the remediation lifecycle without presenting this as an official POA&M for a real federal system.

## POA&M flow

| Step | Action | Example |
|---:|---|---|
| 1 | Identify a weakness or assessment finding | Two modeled user accounts have access not supported by role requirements |
| 2 | Map the finding to the related risk and control | R-001 mapped to AC-6 |
| 3 | Define remediation | Remove unsupported access and review the access-approval or role-change process |
| 4 | Assign an action owner | IAM Team |
| 5 | Set a target date | 2026-09-24 |
| 6 | Track closure evidence | Updated group export, access-review approval, exception correction evidence |
| 7 | Retest or validate | Confirm the two exceptions are corrected and the expected access condition is met |
| 8 | Close only after validation | Mark Closed after closure evidence and retest support the conclusion |

## Status definitions

| Status | Meaning |
|---|---|
| Open | Remediation has not started or is pending action |
| In Progress | Remediation work has started but closure evidence is not complete |
| Pending Validation | Remediation is complete but evidence or retesting still needs review |
| Closed | Remediation and validation are complete and closure evidence is retained |

## Dates

The tracker uses actual modeled target dates rather than relative values such as 30 Days or 60 Days. These are portfolio planning dates, not federal mandated remediation deadlines.

## Closure rule

A remediation action is not considered closed just because the owner says the work is done.

```text
Remediation completed
→ closure evidence received
→ evidence reviewed / retest performed
→ control condition verified
→ item closed
```

> **Note:** This tracker is a portfolio demonstration of remediation-tracking logic. It does not represent an official POA&M for a real federal system.
