# 00 - Project Overview

## The scenario

This project follows a fictional civilian federal environment with internal users, privileged administrators, remote users, business applications, application servers, file shares, logging systems, backup systems, network infrastructure, and segmented network zones.

I kept the scope to five security problems so I could follow each one from risk to control, evidence, remediation, and status without turning the repo into a full federal authorization package.

## The five risk areas

1. excessive user access
2. weak privileged access governance
3. insufficient network segmentation and remote access restrictions
4. incomplete SIEM and logging coverage
5. unvalidated backup and restore processes

Each risk connects to controls that fit the problem, the evidence I would review, and the action needed if the control is not working as expected.

## Frameworks I used

**Main control framework**

- NIST SP 800-53 Rev. 5

**Supporting references**

- NIST SP 800-37 Rev. 2 for risk-management concepts
- NIST SP 800-53A Rev. 5 for assessment methods and terminology
- NIST SP 800-207 for Zero Trust architecture concepts
- CISA Zero Trust Maturity Model for the Zero Trust relationships used in the project

NIST SP 800-53 gives me the controls. NIST SP 800-53A helps with how I assess them. NIST SP 800-37 adds risk-management context. NIST SP 800-207 and the CISA model help connect the work to Zero Trust.

## Where Zero Trust fits

| Area | Zero Trust relationship |
|---|---|
| User and privileged access | Identity |
| Segmentation, inter-zone traffic, and remote access | Networks |
| SIEM coverage and event review | Visibility and Analytics |
| Risk, policy, evidence, and remediation tracking | Governance |

I only use the parts of the Zero Trust models that connect to the work in this repo. I am not assigning maturity levels.

## How the project is organized

| Area | Main files |
|---|---|
| Risk | Risk summary, risk register, risk scoring |
| Controls | Control mapping, security policy |
| Evidence and assessment | Evidence review, access review, access control review |
| Remediation and reporting | Remediation tracker, access retest, remediation validation |

The point is traceability. If I start with one of the five risks, I should be able to follow it into the controls, evidence, remediation, and current status without guessing how the pieces connect.
