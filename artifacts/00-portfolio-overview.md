# 00 - Portfolio Overview

## The scenario

This project uses a fictional civilian federal environment with internal users, privileged administrators, remote access users, application servers, file shares, logging systems, backup systems, network infrastructure, and segmented network zones.

Rather than model an entire agency, I kept the project centered on five security problems that are broad enough to show different parts of GRC work without turning the repo into a full federal authorization package.

## The five risk areas

1. excessive user access
2. weak privileged access governance
3. insufficient network segmentation and remote access restrictions
4. incomplete SIEM and logging coverage
5. unvalidated backup and restore processes

Each risk is tied to the controls that make sense for that problem, the evidence I would expect to review, and the remediation work needed if the condition is not acceptable.

## Frameworks I used

**Primary control framework**

- NIST SP 800-53 Rev. 5

**Supporting references**

- NIST SP 800-37 Rev. 2 for risk-management concepts
- NIST SP 800-53A Rev. 5 for assessment terminology and methods
- NIST SP 800-207 for Zero Trust architecture concepts
- CISA Zero Trust Maturity Model for the Zero Trust relationships used in the project

NIST SP 800-53 does most of the control-mapping work here. The other references help me decide how to assess the controls and how the risk areas relate to Zero Trust.

## Where Zero Trust fits

| Portfolio area | Zero Trust relationship |
|---|---|
| User and privileged access | Identity |
| Segmentation, inter-zone traffic, and remote access | Networks |
| SIEM coverage and event review | Visibility and Analytics |
| Risk, policy, evidence, and remediation tracking | Governance |

I only use the parts of the Zero Trust models that connect to the work in this repo. I am not assigning maturity levels.

## How the project is organized

| Area | Main artifacts |
|---|---|
| Risk | Executive risk summary, risk register, scoring guide |
| Controls | Control mapping matrix, security control policy |
| Evidence and assessment | Evidence checklist, access review data, control assessment |
| Remediation and reporting | POA&M tracker, retest evidence, validation result |

The main thing I wanted the repo to show is traceability: if I start with one of the five risks, I should be able to follow it into the controls, evidence, remediation, and status without having to guess how the pieces connect.
