# 03A - Control Mapping Method

## Purpose

This matrix maps the portfolio risks to selected NIST SP 800-53 Rev. 5 controls. It shows why each control fits the risk, the condition the control is expected to support, and the evidence needed to evaluate that condition.

## Mapping logic

| Step | Action |
|---:|---|
| 1 | Identify the risk condition and affected area |
| 2 | Identify the control family most directly related to the condition |
| 3 | Select the control or enhancement that best addresses the risk |
| 4 | Explain why the control applies |
| 5 | Define the expected control condition |
| 6 | Identify evidence that could support or contradict that condition |
| 7 | Review the evidence when an assessment is performed |
| 8 | Trace confirmed findings to remediation and validation |

## Keep the mapping as narrow as the evidence

A related control is not automatically an assessed control.

The matrix distinguishes between controls that are planned or mapped and controls that have actually been evaluated with evidence. Assessment status is only updated when the available evidence supports testing the stated condition.

## Control precision

When a control enhancement matches the requirement more precisely than the parent control, the enhancement is used.

Example:

```text
Privileged MFA
→ IA-2(1)
```

Configuration management is another example of this distinction:

```text
Approved baseline configuration
→ CM-2

Review and approval of configuration changes
→ CM-3
```

## Implementation type

The `Implementation Type` column is a project-level description of how the control is carried out in the scenario. These are not official NIST control classifications.

| Type | Meaning here |
|---|---|
| Process | Mainly handled through review, approval, ownership, or account management |
| Technical | Mainly configured or enforced through technology |
| Operational | Mainly handled through recurring monitoring, testing, or review |
| Mixed | Uses more than one of the above |

## Traceability rule

Each mapped control should have a clear path back to the risk and forward to the evidence:

```text
Risk
→ Control
→ Expected condition
→ Evidence
→ Assessment result when tested
→ Finding if needed
→ Remediation and validation
```

The matrix is intentionally limited to the controls needed to explain the five portfolio risks rather than attempting to reproduce a full control baseline.
