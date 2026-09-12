# Project Overview

## The scenario

This project follows a fictional civilian federal environment with internal users, privileged administrators, remote users, business applications, application servers, file shares, logging systems, backup systems, network infrastructure, and segmented network zones.

I kept the scope to five security problems so I could follow each one from risk to control, evidence, remediation, and status without turning the repo into a full federal authorization package.

The [System Context](system-context.md) shows how those users, systems, boundaries, logging paths, and recovery components fit together around the five risks.

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

- NIST SP 800-37 Rev. 2 for RMF roles and system-level risk-management context
- NIST SP 800-53A Rev. 5 for assessment methods and terminology
- NIST SP 1308 for Risk Owner and Risk Action Owner terminology and cybersecurity risk accountability
- NIST SP 800-207 for Zero Trust architecture concepts
- CISA Zero Trust Maturity Model for the Zero Trust relationships used in the project

NIST SP 800-53 gives me the controls. NIST SP 800-53A helps with how I assess them. NIST SP 800-37 and NIST SP 1308 add governance and risk-management context. NIST SP 800-207 and the CISA model help connect the work to Zero Trust.

## Governance roles

In this scenario, the **System Owner** is the Risk Owner for the five system-level risks. The technical team responsible for carrying out the selected treatment is the **Risk Action Owner**.

The **System Security Officer (SSO)** coordinates the day-to-day governance work, including the risk register, control mapping, evidence coordination, and POA&M tracking. The **Control Assessor** is responsible for assessment conclusions and remediation validation. The **Authorizing Official (AO)** retains formal authorization and system-level risk acceptance authority.

The [Responsibility Matrix](responsibility-matrix.md) documents how those roles interact without turning every artifact into another ownership table.

## Where Zero Trust fits

| Area | Zero Trust relationship |
|---|---|
| User and privileged access | Identity |
| Segmentation, inter-zone traffic, and remote access | Networks |
| SIEM coverage and event review | Visibility and Analytics |
| Risk, policy, evidence, and remediation tracking | Governance |

I only use the parts of the Zero Trust models that connect to the work in this repo. I am not assigning maturity levels.

## How the project is organized

| Work area | What it contains |
|---|---|
| Context and Governance | System context, policy, governance roles, and responsibility matrix |
| Risk and Controls | Risk analysis, scoring, register, executive view, and control mapping |
| Assessment and Evidence | Evidence planning, source data, assessment narrative, and workpaper |
| Remediation and Validation | POA&M process, tracker, retest evidence, and closure validation |

The point is traceability. If I start with one of the five risks, I should be able to follow it into ownership, controls, evidence, assessment results, remediation, and current status without guessing how the pieces connect.
