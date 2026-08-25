# 00 - Portfolio Overview

## Document control

| Field | Value |
|---|---|
| Document | Federal Zero Trust GRC Portfolio Overview |
| Project Type | Graduate Capstone-Derived GRC Portfolio Project |
| Author | Mark C. |
| Version | 1.2 |
| Disclaimer | For portfolio demonstration purposes only. This project is derived from a graduate cybersecurity capstone and does not contain sensitive, proprietary, or real federal agency data. |

## Project background

This portfolio focuses on unauthorized-access risk in a modeled civilian federal environment.

The modeled environment includes internal users, privileged administrators, remote access users, application servers, file shares, logging systems, backup systems, network infrastructure, and segmented network zones.

The work was reorganized into GRC artifacts so the reasoning can be followed from an identified condition through risk analysis, control selection, evidence review, a finding, and remediation tracking.

## Scope

The portfolio covers five risk themes:

1. excessive user access
2. weak privileged access governance
3. insufficient network segmentation and remote-access restrictions
4. incomplete SIEM and logging coverage
5. unvalidated backup and restore processes

The purpose is not to model every control or every RMF activity. The scope is intentionally limited so each artifact has a clear reason to exist.

## Framework use

### Primary control framework

- NIST SP 800-53 Rev. 5

### Supporting references

- NIST SP 800-37 Rev. 2 Risk Management Framework concepts
- NIST SP 800-53A Rev. 5 assessment terminology and methods
- NIST SP 800-207 Zero Trust Architecture
- CISA Zero Trust Maturity Model

NIST SP 800-53 is the main source for control selection. The other references help frame assessment, risk-management, and selected Zero Trust concepts.

This is not presented as a complete RMF Select, Assess, Authorize, or Monitor package.

## Method used

The working method is:

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

The modeled access-review exercise demonstrates that full chain for R-001 and AC-6.

## Selected Zero Trust relationship

| Portfolio work | Zero Trust relationship |
|---|---|
| User and privileged access | Identity |
| Segmentation, inter-zone traffic, and remote access | Networks |
| SIEM coverage and event review | Visibility and Analytics |
| Risk, policy, evidence, and remediation tracking | Governance |

This is a limited crosswalk only. It does not assign maturity levels or claim full coverage of the CISA model.

## Portfolio boundaries

This project does not claim to include:

- a complete system categorization
- a full control baseline selection and tailoring package
- an SSP
- an SAP or SAR
- an authorization decision
- a continuous monitoring program
- a full Zero Trust maturity assessment

Residual risk is not calculated across the environment because control effectiveness and remediation have not been validated across the full scope.

## What the modeled assessment does prove

The synthetic access-review exercise is limited to one condition: whether observed access matches approved role access.

That is used as a focused AC-6 Least Privilege assessment example. AC-2 Account Management is related to the broader account lifecycle, but the modeled access-review exercise does not claim to assess the full AC-2 control.
