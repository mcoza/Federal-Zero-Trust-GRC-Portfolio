# 03A - Control Mapping Method

## Purpose

This matrix maps identified portfolio risks to selected NIST SP 800-53 Rev. 5 controls. The goal is to show why a control is relevant to a risk, what good implementation should look like, and what evidence would support an assessment.

This is not presented as a complete RMF Select step. A full Select step would involve baseline selection, tailoring, allocation, and related system documentation. This portfolio is narrower and focuses on risk-to-control reasoning.

## Mapping logic

| Step | Action | Example |
|---:|---|---|
| 1 | Identify the risk condition | Excessive user access |
| 2 | Identify the control family that addresses the condition | AC - Access Control |
| 3 | Select the most relevant control or enhancement | AC-6 Least Privilege |
| 4 | Explain why the control applies | The risk is caused by access exceeding role requirements |
| 5 | Define the expected implementation | User permissions match approved role and business need |
| 6 | Identify evidence | RBAC matrix, group membership export, access review notes |
| 7 | Assess the evidence when available | Compare observed access to approved access |
| 8 | Trace exceptions to remediation | Assessment finding to POA&M item and retest evidence |

## Control precision

Where the expected implementation depends on a specific control enhancement, the matrix uses the enhancement rather than only the parent control.

Example:

```text
Privileged MFA
→ IA-2(1)
```

rather than using IA-2 alone when the specific requirement being discussed is multi-factor authentication for privileged accounts.

## Control type definitions

| Control type | Description | Examples |
|---|---|---|
| Management / Administrative | Policy, governance, planning, review, ownership, and risk decision controls | Policies, access reviews, POA&M tracking, risk decisions |
| Technical | Controls configured or enforced through technology | MFA, firewall rules, logging configuration, segmentation, access restrictions |
| Operational | Recurring human or process-driven security activities | Log review, backup testing, access review execution, evidence collection |

## Traceability rule

A control should not appear in an evidence checklist without a clear reason upstream. The intended chain is:

```text
Risk
→ Control
→ Expected implementation
→ Evidence
→ Assessment result
→ Finding if needed
→ Remediation
```

Remote access is therefore tied to R-003 through AC-17 rather than appearing only as a standalone evidence item.
