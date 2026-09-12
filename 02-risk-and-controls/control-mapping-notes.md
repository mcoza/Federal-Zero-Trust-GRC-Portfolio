# Control Mapping Notes

## How I map controls

I start with the risk, not the control catalog.

The control mapping answers four basic questions:

1. What is the risk?
2. Which NIST control fits the problem?
3. What should I actually check?
4. What evidence would help me answer that question?

## My process

| Step | What I do |
|---:|---|
| 1 | Define the problem I am trying to address |
| 2 | Choose the control or enhancement that best fits it |
| 3 | State in plain language what should be true if the control is working |
| 4 | Identify the evidence I would review |
| 5 | Document the result if I actually test the control |
| 6 | Send confirmed findings into remediation and retesting |

## Related does not mean assessed

A control can be related to a risk without being tested.

I only treat a control as assessed when I have evidence that lets me evaluate the condition I wrote for it. If the evidence is narrow, the conclusion stays narrow too.

The control mapping itself is not a status tracker. The completed R-001 / AC-6 assessment is documented in the [Access Control Review](../03-assessment-and-evidence/access-control-review.md), and the follow-up retest is documented in [Remediation Validation](../04-remediation-and-validation/remediation-validation.md).

## Using the most specific control that fits

When an enhancement fits the requirement better than the parent control, I use the enhancement.

For example:

```text
Privileged MFA
→ IA-2(1)
```

For configuration management:

```text
Approved baseline configuration
→ CM-2

Review and approval of configuration changes
→ CM-3
```

## Cross-cutting remediation tracking

I use CA-5 Plan of Action and Milestones as a supporting reference for remediation tracking across the project. I do not assign it to one specific risk in the control mapping because it governs how findings are tracked and closed rather than mitigating one risk condition by itself.

## What I want to be able to trace

```text
Risk
→ control
→ what should be true
→ evidence
→ assessment result
→ finding, if there is one
→ remediation
→ retest
```

If I cannot explain that chain, the mapping needs more work.

The file only includes controls tied directly to the five risk conditions in this project. It is not meant to be a full NIST control baseline.
