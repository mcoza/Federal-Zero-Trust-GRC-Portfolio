# 02A - Risk Scoring

## How I score the risks

I use a simple 5x5 likelihood and impact model so I can rank the five risks consistently.

**Formula:** `Initial Risk Score = Likelihood × Impact`

The score helps me compare priorities. It is not a statistical prediction.

The number matters less than the reasoning behind it, so every risk in the register includes a short explanation for both likelihood and impact.

## Likelihood

| Score | Likelihood | How I use it |
|---:|---|---|
| 1 | Rare | Unlikely under normal conditions |
| 2 | Unlikely | Possible, but not expected |
| 3 | Possible | Could happen in some circumstances |
| 4 | Likely | Has a reasonable chance of happening |
| 5 | Almost Certain | Expected to happen frequently or repeatedly |

## Impact

| Score | Impact | How I use it |
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

These rating bands are defined for this project. They are not NIST-required thresholds. I use them consistently so the five risks can be compared the same way.

## The two questions I use

1. **Likelihood:** Given the weakness and the threat path, how likely is the risk event?
2. **Impact:** If it happens, how bad could the security, operational, recovery, or compliance impact be?

The score helps sort the risks. The rationale explains why the score makes sense.

## Residual risk

I would only rescore a risk after there is evidence that the treatment actually changed the condition. A planned fix or the closure of one narrow finding is not enough by itself to assign residual risk.
