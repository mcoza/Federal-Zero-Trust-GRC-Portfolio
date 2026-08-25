# 03A - Control Mapping Method

## Purpose

This matrix maps the portfolio risks to selected NIST SP 800-53 Rev. 5 controls. I use it to show why a control fits a risk, what I expect the control to do, and what evidence I would need to check it.

I am only showing the control mapping needed for this portfolio, not the full RMF Select process.

## Mapping logic

| Step | Action | Example |
|---:|---|---|
| 1 | Identify the risk condition | Excessive user access |
| 2 | Identify the control family | AC - Access Control |
| 3 | Select the most relevant control or enhancement | AC-6 Least Privilege |
| 4 | Explain why it applies | The risk comes from access exceeding role requirements |
| 5 | Define the expected condition | User permissions match approved role and business need |
| 6 | Identify evidence | Approved role matrix, group membership export, access review results |
| 7 | Review the evidence when available | Compare observed access with approved access |
| 8 | Trace exceptions to remediation | Assessment finding to POA&M item and retest evidence |

## Keep the mapping as narrow as the evidence

I only mark a control as assessed when the evidence actually tests that control condition.

The access review compares approved access with observed access, so that assessment is scoped to AC-6 Least Privilege.

AC-2 Account Management is related to account lifecycle and review, but the access review dataset does not test the full AC-2 lifecycle. I do not mark AC-2 as assessed from that exercise.

## Control precision

When a specific control enhancement matches the requirement better than the parent control, I use the enhancement.

Example:

```text
Privileged MFA
→ IA-2(1)
```

## Implementation type

The `Implementation Type` column is just a quick description of how the control is carried out in this scenario. These are not official NIST control classifications.

| Type | Meaning here |
|---|---|
| Process | Mainly handled through review, approval, ownership, or account management |
| Technical | Mainly configured or enforced through technology |
| Operational | Mainly handled through recurring monitoring, testing, or review |
| Mixed | Uses more than one of the above |

## Traceability rule

A control should have a clear reason for being there. I use this chain:

```text
Risk
→ Control
→ Expected condition
→ Evidence
→ Assessment result
→ Finding if needed
→ Remediation
```

Remote access is tied to R-003 through AC-17 instead of appearing only in the evidence checklist.