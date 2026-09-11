# 02A - Risk Scoring Guide

## How I score the risks

I use a basic 5x5 likelihood and impact model to keep the ranking consistent across the five risks.

**Formula:** `Initial Risk Score = Likelihood × Impact`

The score is a starting point, not a statistical prediction. I use it to compare the risks in this scenario before the recommended fixes are completed and validated.

The number matters less than the reasoning behind it, so every risk in the register includes a short explanation for both likelihood and impact.

## Likelihood

| Score | Likelihood | What I mean by it |
|---:|---|---|
| 1 | Rare | Unlikely under normal conditions |
| 2 | Unlikely | Possible, but not expected |
| 3 | Possible | Could happen in some circumstances |
| 4 | Likely | Has a reasonable chance of happening |
| 5 | Almost Certain | Expected to happen frequently or repeatedly |

## Impact

| Score | Impact | What I mean by it |
|---:|---|---|
| 1 | Minimal | Limited operational, security, or compliance effect |
| 2 | Minor | Some disruption or a relatively small control weakness |
| 3 | Moderate | Noticeable operational, security, or compliance impact |
| 4 | Major | Significant access, operational, recovery, or compliance impact |
| 5 | Severe | Serious unauthorized access, data exposure, mission disruption, or audit failure risk |

## Ratings

| Score range | Rating |
|---|---|
| 1-8 | Low |
| 9-14 | Moderate |
| 15-25 | High |

## The two questions I use

1. **Likelihood:** Given the weakness and the threat path, how likely is the risk event in this scenario?
2. **Impact:** If it happens, how bad could the security, operational, recovery, or compliance impact be?

That keeps the scoring simple enough to explain and consistent enough to prioritize the work.

## Residual risk

I would only rescore a risk after there is evidence that the treatment actually changed the condition. A planned fix—or closing one narrow finding—is not enough by itself to say what the residual risk is.
