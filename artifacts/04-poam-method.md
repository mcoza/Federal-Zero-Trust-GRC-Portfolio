# 04A - POA&M Method

## Purpose

This tracker records findings, related risks and controls, remediation work, action owners, target dates, status, and closure evidence.

## POA&M flow

| Step | Action | Example |
|---:|---|---|
| 1 | Identify a weakness or assessment finding | Two user accounts have access not supported by role requirements |
| 2 | Map the finding to the related risk and control | R-001 mapped to AC-6 |
| 3 | Define remediation | Remove unsupported access and review the access approval or role change process |
| 4 | Assign an action owner | IAM Team |
| 5 | Set a target date | 2026-09-24 |
| 6 | Track closure evidence | Updated group export, access review approval, exception correction evidence |
| 7 | Retest or validate | Confirm the two exceptions are corrected and the expected access condition is met |
| 8 | Close only after validation | Mark Closed after the evidence and retest support closure |

## Status definitions

| Status | Meaning |
|---|---|
| Open | Remediation has not started or is waiting for action |
| In Progress | Remediation has started but closure evidence is not complete |
| Pending Validation | Remediation is complete but the evidence or retest still needs review |
| Closed | Remediation and validation are complete and closure evidence is retained |

## Dates

The tracker uses example target dates instead of relative values such as 30 Days or 60 Days. These dates are for the portfolio. They are not federal deadlines.

## Closure rule

A remediation item is not closed just because the owner says the work is done.

```text
Remediation completed
→ closure evidence received
→ evidence reviewed or retest performed
→ control condition verified
→ item closed
```
