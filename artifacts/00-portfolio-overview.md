# 00 - Portfolio Overview

## Document control

| Field | Value |
|---|---|
| Document | Federal Zero Trust GRC Portfolio Overview |
| Project Type | Graduate Capstone GRC Portfolio Project |
| Author | Mark C. |
| Version | 1.5 |

## Project background

This portfolio focuses on unauthorized access risk in a fictional civilian federal environment.

The environment includes internal users, privileged administrators, remote access users, application servers, file shares, logging systems, backup systems, network infrastructure, and segmented network zones.

I reorganized the capstone into GRC artifacts so you can follow how I got from a security issue to the risk, controls, evidence, finding, remediation, and validation.

## Scope

The portfolio covers five risk themes:

1. excessive user access
2. weak privileged access governance
3. insufficient network segmentation and remote access restrictions
4. incomplete SIEM and logging coverage
5. unvalidated backup and restore processes

The scope is intentionally limited so the artifacts can show the reasoning and traceability across each stage of the assessment process.

## Framework use

### Primary control framework

- NIST SP 800-53 Rev. 5

### Supporting references

- NIST SP 800-37 Rev. 2 Risk Management Framework concepts
- NIST SP 800-53A Rev. 5 assessment terminology and methods
- NIST SP 800-207 Zero Trust Architecture
- CISA Zero Trust Maturity Model

NIST SP 800-53 is the main source I use for control selection. The other references help with assessment, risk management, and the Zero Trust concepts used in the project.

## Method used

My working process is:

```text
Identify condition
→ write the risk
→ score likelihood and impact with rationale
→ select the control that addresses the condition
→ define the expected control condition
→ identify evidence
→ compare evidence with the condition
→ document a conclusion or finding
→ track remediation
→ validate before closure
```

The access review and remediation retest show that full chain for R-001 and the scoped AC-6 condition.

## Selected Zero Trust relationship

| Portfolio work | Zero Trust relationship |
|---|---|
| User and privileged access | Identity |
| Segmentation, inter-zone traffic, and remote access | Networks |
| SIEM coverage and event review | Visibility and Analytics |
| Risk, policy, evidence, and remediation tracking | Governance |

The crosswalk shows only the relationships used in this project; no maturity levels are assigned.

## Residual risk

Residual risk is not calculated across the environment because the relevant controls have not been validated across the full scope. Closing one scoped finding is not enough to establish residual risk for the broader environment.

## Assessment scope

The synthetic access review assesses whether observed access matches approved role access for the scoped AC-6 condition.

AC-2 Account Management is related to the broader account lifecycle, but it is not assessed by this exercise.

The remediation retest validates correction of the two unsupported group memberships identified in the original assessment. Broader AC-6 effectiveness remains outside the scope of that retest.
