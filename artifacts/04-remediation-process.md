# 04A - Remediation Process

## How I use the tracker

The remediation tracker is where a weakness turns into owned corrective work.

For each item, I want to know what the problem is, what risk and control it ties back to, who owns the fix, what has to happen before closure, and what evidence proves the work is actually done.

The `Finding Source` field also matters. Some items came from a completed control review, while others are weaknesses built into the scenario. I keep those separate so the tracker does not make it look like I tested controls that I did not test.

## The flow

| Step | What happens |
|---:|---|
| 1 | Identify the weakness or assessment finding |
| 2 | Tie it back to the related risk and control |
| 3 | Define the corrective action |
| 4 | Assign an owner |
| 5 | Set milestones and a target date |
| 6 | Collect evidence that the work was completed |
| 7 | Review the evidence or retest the condition |
| 8 | Close the item when the scoped fix is supported by evidence |

## Statuses

| Status | Meaning |
|---|---|
| Open | Work has not started or is waiting for action |
| In Progress | Work has started, but the item is not ready for validation |
| Pending Validation | The fix is complete and waiting for evidence review or retest |
| Closed | The fix was validated and the closure evidence is retained |

## Dates

I use specific dates so the items read like real tracked work instead of vague “30-day” or “60-day” placeholders. The dates are part of the scenario, not universal federal deadlines.

## What counts as closed

An item is not closed just because the owner says it is fixed.

```text
Fix completed
→ closure evidence received
→ evidence reviewed or retest performed
→ condition verified
→ item closed
```

That closure only applies to the weakness being tracked. It does not automatically mean the larger risk is gone or that the residual risk is acceptable.
