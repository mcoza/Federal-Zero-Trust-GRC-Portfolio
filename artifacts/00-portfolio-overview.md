# 00 - Portfolio Overview

## Document control

| Field | Value |
|---|---|
| Document | Federal Zero Trust GRC Portfolio Overview |
| Project Type | Graduate Capstone GRC Portfolio Project |
| Author | Mark C. |
| Version | 1.3 |
| Disclaimer | For portfolio demonstration purposes only. This project is based on a graduate cybersecurity capstone and does not contain sensitive, proprietary, or real federal agency data. |

## Project background

This portfolio focuses on unauthorized access risk in a fictional civilian federal environment.

The environment includes internal users, privileged administrators, remote access users, application servers, file shares, logging systems, backup systems, network infrastructure, and segmented network zones.

I reorganized the capstone into GRC artifacts so you can follow how I got from a security issue to the risk, controls, evidence, finding, and remediation.

## Scope

The portfolio covers five risk themes:

1. excessive user access
2. weak privileged access governance
3. insufficient network segmentation and remote access restrictions
4. incomplete SIEM and logging coverage
5. unvalidated backup and restore processes

I kept the scope small on purpose. The goal is to show the full reasoning process, not recreate an entire federal RMF package.

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

The access review exercise shows that full chain for R-001 and AC-6.

## Selected Zero Trust relationship

| Portfolio work | Zero Trust relationship |
|---|---|
| User and privileged access | Identity |
| Segmentation, inter-zone traffic, and remote access | Networks |
| SIEM coverage and event review | Visibility and Analytics |
| Risk, policy, evidence, and remediation tracking | Governance |

This is only a limited crosswalk. I am not assigning maturity levels or claiming full coverage of the CISA model.

## What this project does not cover

This project does not include:

- a complete system categorization
- a full control baseline selection and tailoring package
- an SSP
- an SAP or SAR
- an authorization decision
- a continuous monitoring program
- a full Zero Trust maturity assessment

I also do not calculate residual risk across the environment because the controls and remediation have not been validated across the full scope.

## What the access review actually tests

The synthetic access review checks one condition: whether observed access matches approved role access.

I use that as a focused AC-6 Least Privilege assessment example. AC-2 Account Management is related to the broader account lifecycle, but this exercise does not test the full AC-2 control.