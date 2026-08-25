# 02A - Risk Scoring Guide

## Risk scoring method

This portfolio uses a simple 5x5 likelihood and impact model to support prioritization.

**Formula:** `Inherent Risk Score = Likelihood × Impact`

Inherent risk represents the modeled risk level before additional remediation is validated.

The numbers are not meant to represent statistical probabilities. They are analyst judgments based on the modeled condition, affected area, threat path, and expected consequence. Each risk-register entry includes a short likelihood and impact rationale so another reviewer can see why the score was chosen.

## Likelihood scale

| Score | Likelihood | Description |
|---:|---|---|
| 1 | Rare | Unlikely to occur under normal conditions |
| 2 | Unlikely | Could occur, but not expected |
| 3 | Possible | Could occur in some circumstances |
| 4 | Likely | Expected to occur or has a reasonable chance of occurring |
| 5 | Almost Certain | Expected to occur frequently or repeatedly |

## Impact scale

| Score | Impact | Description |
|---:|---|---|
| 1 | Minimal | Limited operational, security, or compliance impact |
| 2 | Minor | Some disruption or minor control weakness |
| 3 | Moderate | Noticeable operational, security, or compliance impact |
| 4 | Major | Significant access, operational, recovery, or compliance impact |
| 5 | Severe | Serious unauthorized access, data exposure, mission disruption, or audit failure risk |

## Risk rating scale

| Score range | Rating |
|---|---|
| 1-8 | Low |
| 9-14 | Moderate |
| 15-25 | High |

## Scoring rule used in this portfolio

For each risk, I ask two separate questions:

1. **Likelihood:** Given the modeled weakness and threat path, how plausible is the event or condition?
2. **Impact:** If it occurs, how serious is the security, operational, recovery, or compliance consequence?

I record the rationale before relying on the numeric score. The score helps rank the risks, but the written rationale is what makes the judgment reviewable.

## Residual risk

This portfolio does not assign residual-risk scores just because a control or remediation is planned. Residual risk should be reconsidered after there is evidence about implementation, control effectiveness, and remediation results.
