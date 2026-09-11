# 04A - Remediation Process

## How I use the tracker

The remediation tracker turns a problem into work with an owner, target date, evidence, and a closure decision.

For each item, I want to know what the problem is, which risk and controls it ties back to, who owns the fix, what has to happen before closure, and what evidence shows the work is done.

The `Source` field matters too. Some items came from a completed control review. Others are issues built into the scenario that have not been tested yet. Keeping those separate stops the tracker from implying more testing than actually happened.

## The flow

| Step | What happens |
|---:|---|
| 1 | Identify the issue or assessment finding |
| 2 | Tie it to the related risk and controls |
| 3 | Define the corrective action |
| 4 | Assign an owner |
| 5 | Set milestones and a target date |
| 6 | Collect evidence that the work was completed |
| 7 | Review the evidence or retest the condition |
| 8 | Close the item when the fix is supported by evidence |

## Statuses

| Status | Meaning |
|---|---|
| Open | Work has not started or is waiting for action |
| In Progress | Work has started, but the item is not ready for validation |
| Pending Validation | The fix is complete and waiting for evidence review or retest |
| Closed | The fix was validated and the closure evidence is retained |

## Dates

I use specific dates instead of vague 30-day or 60-day placeholders. The dates belong to this scenario and are not universal federal deadlines.

## What counts as closed

An item is not closed just because the owner says it is fixed.

```text
Fix completed
→ closure evidence received
→ evidence reviewed or retest performed
→ condition verified
→ item closed
```

Closure applies to the issue being tracked. It does not automatically close the larger risk or establish an acceptable residual risk.
