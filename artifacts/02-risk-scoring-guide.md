# 02A - Risk Scoring Guide

## Risk scoring method

This portfolio uses a simple 5x5 likelihood and impact model to rank risks.

**Formula:** `Inherent Risk Score = Likelihood × Impact`

Inherent risk is the level of risk before additional remediation is validated.

The numbers are not statistical probabilities. They are judgments based on the condition, affected area, threat path, and expected impact. Each risk in the register includes a short explanation for the likelihood and impact scores.

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

## How I score each risk

I ask two questions:

1. **Likelihood:** Given the weakness and threat path, how likely is this to happen?
2. **Impact:** If it happens, how serious would the security, operational, recovery, or compliance impact be?

I include the written rationale so someone else can see why I chose the score. The number helps rank the risks, but the explanation matters more than the number by itself.

## Residual risk

I would only score residual risk after I had evidence that the controls were implemented and working. A planned fix by itself is not enough.