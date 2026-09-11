# 05A - Responsibility Matrix (RACI)

## Purpose

This matrix separates accountability from execution so that Risk Owner, Risk Action Owner, Remediation Owner, Control Owner, and Evidence Owner do not all mean the same thing.

For the five system-level risks in this scenario:

- the **System Owner** is the Risk Owner
- the technical team named in the risk register is the **Risk Action Owner**
- the **System Security Officer (SSO)** coordinates the governance work and POA&M tracking
- the **Control Assessor** is responsible for assessment conclusions and remediation validation
- the **Authorizing Official (AO)** makes formal authorization and system-level risk acceptance decisions

## RACI key

| Letter | Meaning |
|---|---|
| R | Responsible for doing the work |
| A | Accountable for the activity or outcome |
| C | Consulted before or during the work |
| I | Informed of the activity or result |
| A/R | The same role both performs the work and is accountable for the result |

## Matrix

| Activity | AO | System Owner | SSO | Control Assessor | IAM | Security / IAM | Network | SOC | SysAdmin |
|---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Maintain system risk register | I | A | R | C | C | C | C | C | C |
| Control mapping and evidence planning | I | A | R | C | C | C | C | C | C |
| Security policy maintenance | I | A | R | I | C | C | C | C | C |
| User access review | I | A | C | I | R | C | I | I | I |
| Privileged access governance | I | A | C | I | C | R | I | C | I |
| Network segmentation and remote access | I | A | C | I | I | C | R | C | I |
| Logging and SIEM coverage | I | A | C | I | I | C | C | R | I |
| Backup and restore testing | I | A | C | I | I | I | I | I | R |
| Control assessment | I | C | C | A/R | C | C | C | C | C |
| POA&M preparation and tracking | I | A | R | C | C | C | C | C | C |
| Remediation validation or retest | I | C | C | A/R | C | C | C | C | C |
| Authorization and system-level risk acceptance | A/R | C | C | C | I | I | I | I | I |

## How I apply it to remediation

The Risk Action Owner for a risk is the default Remediation Owner when a POA&M item is assigned to that team, unless the corrective action is reassigned.

That means the current remediation ownership follows the same domain split as the risk register:

| Risk | Risk Action Owner / default Remediation Owner |
|---|---|
| R-001 Excessive user access | IAM Team |
| R-002 Privileged access governance | Security / IAM Team |
| R-003 Insufficient network segmentation | Network Team |
| R-004 Incomplete SIEM/logging coverage | SOC Team |
| R-005 Unvalidated backup and restore | SysAdmin Team |

The AO is not the day-to-day owner of these actions. The AO becomes relevant when a formal authorization or system-level risk acceptance decision is required.
