# 04A - Remediation Process

## How I use the tracker

The remediation tracker turns an issue into work with an owner, target date, closure requirements, and evidence.

For each item, I want to know what the problem is, which risk and controls it ties back to, who owns the fix, what has to happen before closure, and what evidence supports the closure decision.

## Source matters

The `Source` field separates tested findings from conditions that are part of the scenario baseline.

- **Assessment finding:** came from a completed control review.
- **Scenario baseline:** an assumed starting condition in the fictional environment that has not been tested yet.

That distinction keeps the tracker from implying that every open item came from a completed assessment.

The `Related Controls` field shows which controls connect to the issue. It does not mean those controls were assessed.

## The flow

| Step | What happens |
|---:|---|
| 1 | Identify the issue or assessment finding |
| 2 | Tie it to the related risk and controls |
| 3 | Define the corrective action |
| 4 | Assign a remediation owner |
| 5 | Set milestones and a target date |
| 6 | Define what must be true before the item can close |
| 7 | Collect and review evidence or retest the condition |
| 8 | Close the item when the requirements are met and supported by evidence |

## Closure requirements and evidence

`Closure Requirements` describes what has to be true before an item can close.

`Closure Evidence` lists the evidence that actually supports a closed item. Open items leave this field blank because the evidence has not been produced or validated yet.

That keeps planned work separate from completed work.

## Statuses

| Status | Meaning |
|---|---|
| Open | Work has not started or is waiting for action |
| In Progress | Work has started, but the item is not ready for validation |
| Pending Validation | The fix is complete and waiting for evidence review or retest |
| Closed | The closure requirements were met and supported by evidence |

## Dates

I use specific dates instead of vague 30-day or 60-day placeholders. The dates belong to this scenario and are not universal federal deadlines.

## What counts as closed

An item is not closed just because the owner says it is fixed.

```text
Fix completed
→ closure requirements met
→ evidence reviewed or retest performed
→ condition verified
→ closure evidence retained
→ item closed
```

Closure applies to the issue being tracked. It does not automatically close the larger risk or establish an acceptable residual risk.
