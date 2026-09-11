# 02A - Risk Scoring Guide

## Risk scoring method

This portfolio uses a simple 5x5 likelihood and impact model to rank risks.

**Formula:** `Initial Risk Score = Likelihood × Impact`

The initial risk score reflects the scenario conditions before the recommended treatment actions are completed and validated. It is used to prioritize the risks in this project; it is not intended to represent a statistical probability or a formal enterprise risk model.

Each risk in the register includes a short explanation for the likelihood and impact scores so the reasoning can be reviewed alongside the number.

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

1. **Likelihood:** Given the weakness and threat path, how likely is the risk event under the scenario conditions?
2. **Impact:** If it occurs, how serious would the security, operational, recovery, or compliance impact be?

The number helps rank the risks, but the written rationale matters more than the number by itself.

## Residual risk

Residual risk would be considered after relevant treatment actions are implemented and there is evidence showing how the control environment changed. A planned remediation or the closure of one narrow finding is not enough by itself to determine the broader residual risk.
