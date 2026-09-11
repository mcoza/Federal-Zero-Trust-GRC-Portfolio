# 03A - Control Mapping Notes

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

I only mark a control as assessed when I have evidence that lets me evaluate the condition I wrote for it. If the evidence is narrow, the conclusion stays narrow too.

That keeps the mapping from looking more complete than the work behind it.

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

The file only includes controls tied to the five risks in this project. It is not meant to be a full NIST control baseline.
