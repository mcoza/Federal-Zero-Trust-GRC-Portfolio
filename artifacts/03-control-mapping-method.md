# 03A - Control Mapping Method

## How I map controls

I start with the risk, not the control catalog.

For each risk, I look at the actual condition I am trying to address, choose the NIST SP 800-53 control that fits it best, then decide what evidence I would need to see before I could say anything meaningful about that control.

## My process

| Step | What I do |
|---:|---|
| 1 | Define the risk condition and the area it affects |
| 2 | Find the control family that is most relevant |
| 3 | Pick the control or enhancement that best fits the problem |
| 4 | Explain why that control belongs |
| 5 | Write the condition I would expect to see if the control is working |
| 6 | Identify evidence that could support or contradict that condition |
| 7 | Review the evidence when I actually assess the control |
| 8 | Send confirmed findings into remediation and validation |

## Related does not mean assessed

A control can be related to a risk without being tested.

I only mark a control as assessed when the evidence actually lets me evaluate the condition I wrote for it. If the evidence is too narrow, the assessment stays narrow too.

That distinction matters because it is easy to make a control matrix look more complete than the work behind it really is.

## Using the most specific control that fits

When an enhancement fits the requirement better than the parent control, I use the enhancement.

For example:

```text
Privileged MFA
→ IA-2(1)
```

And for configuration management:

```text
Approved baseline configuration
→ CM-2

Review and approval of configuration changes
→ CM-3
```

## Implementation type

The `Implementation Type` column is just a shorthand I use in this project. It is not an official NIST classification.

| Type | Meaning here |
|---|---|
| Process | Mostly handled through review, approval, ownership, or account management |
| Technical | Mostly configured or enforced through technology |
| Operational | Mostly handled through recurring monitoring, testing, or review |
| Mixed | Uses more than one of the above |

## What I want to be able to trace

```text
Risk
→ control
→ expected condition
→ evidence
→ assessment result
→ finding, if there is one
→ remediation
→ validation
```

If I cannot explain that chain, the mapping probably needs more work.

I kept the matrix to the controls needed for the five risks in this repo instead of trying to build a full NIST control baseline.
