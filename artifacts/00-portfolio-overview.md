# 00 - Portfolio Overview

## Document control

| Field | Value |
|---|---|
| Document | Federal Zero Trust GRC Portfolio Overview |
| Project Type | Graduate Capstone GRC Portfolio Project |
| Author | Mark C. |
| Version | 1.6 |

## Project background

This portfolio evaluates security and control risk in a fictional civilian federal environment.

The environment includes internal users, privileged administrators, remote access users, application servers, file shares, logging systems, backup systems, network infrastructure, and segmented network zones.

The capstone material is organized into GRC artifacts so the relationships between risks, controls, evidence, remediation, and reporting are visible across the project.

## Scope

The portfolio covers five risk themes:

1. excessive user access
2. weak privileged access governance
3. insufficient network segmentation and remote access restrictions
4. incomplete SIEM and logging coverage
5. unvalidated backup and restore processes

The scope is intentionally limited so each risk can be traced to relevant controls, evidence expectations, treatment actions, and status.

## Framework use

### Primary control framework

- NIST SP 800-53 Rev. 5

### Supporting references

- NIST SP 800-37 Rev. 2 Risk Management Framework concepts
- NIST SP 800-53A Rev. 5 assessment terminology and methods
- NIST SP 800-207 Zero Trust Architecture
- CISA Zero Trust Maturity Model

NIST SP 800-53 is the main source for control selection. The supporting references inform assessment methods, risk-management concepts, and the Zero Trust relationships used in the project.

## Selected Zero Trust relationships

| Portfolio work | Zero Trust relationship |
|---|---|
| User and privileged access | Identity |
| Segmentation, inter-zone traffic, and remote access | Networks |
| SIEM coverage and event review | Visibility and Analytics |
| Risk, policy, evidence, and remediation tracking | Governance |

The crosswalk reflects only the relationships represented in the project; no maturity levels are assigned.

## Project structure

The portfolio is organized around four connected layers:

| Layer | Main artifacts |
|---|---|
| Risk | Executive risk summary, risk register, scoring guide |
| Controls | Control mapping matrix, security control policy |
| Evidence and assessment | Evidence checklist, access review data, control assessment |
| Remediation and reporting | POA&M tracker, retest evidence, validation result |

This structure keeps the project centered on traceability from the identified risks to the controls and evidence used to manage them.
