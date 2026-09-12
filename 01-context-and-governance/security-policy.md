# Security Policy

## Document control

| Field | Value |
|---|---|
| Document | Security Policy |
| Project | Federal Zero Trust GRC Portfolio |
| Author | Mark C. |
| Version | 1.0 |
| Policy Owner | System Security Officer (SSO) |
| Approval Authority | System Owner |
| Effective Date | 2026-08-25 |
| Review Cycle | Annual or after major system change |

## Purpose

This policy defines security requirements for user access, privileged access, network segmentation, remote access, logging and monitoring, backup validation, and exceptions.

## Scope

This policy applies to the fictional federal environment used in this project, including internal users, privileged users, remote access users, business applications, application servers, file shares, administrative systems, network infrastructure, SIEM/logging systems, backup systems, and DMZ systems.

## Roles and responsibilities

| Role / Team | Responsibility |
|---|---|
| Authorizing Official (AO) | Makes formal system authorization and system-level risk acceptance decisions |
| System Owner | Serves as Risk Owner for the five system-level risks and is accountable for treatment, system requirements, and system-specific policy |
| System Security Officer (SSO) | Maintains the operational security posture and coordinates the risk register, control mapping, evidence, exceptions, and POA&M tracking |
| Control Assessor | Assesses selected controls and validates remediation or retests with the degree of independence required by the organization |
| IAM Team | Manages user access, access reviews, and account changes |
| Security / IAM Team | Manages privileged access requirements and MFA |
| Network Team | Manages segmentation, firewall and ACL rules, and approved remote access paths |
| SOC Team | Manages required security logging, monitoring, and review activity |
| SysAdmin Team | Manages backup jobs and restore testing |

The detailed responsibility split is documented in the [Responsibility Matrix](responsibility-matrix.md).

## Policy requirements

### Role-based access

Access to systems and data must be based on documented job role requirements. Users must be granted only the access needed for approved business functions.

### Access reviews

User and privileged access must be reviewed on a scheduled basis and after significant role changes. Access that is no longer required must be removed or modified.

### Privileged access

Privileged accounts must be separated from standard user accounts where applicable. Privileged access must require multi-factor authentication and must be monitored through available logging and SIEM capabilities.

### Network segmentation

The internal network must be separated into defined zones where applicable, including user, server, administrative, remote access, DMZ, logging, and backup zones.

### Inter-zone traffic

Traffic between network zones must be denied by default and allowed only when there is a documented business requirement, an approved owner, and a logging requirement where feasible.

### Remote access

Remote access must use approved authentication methods, be limited to authorized users, and provide only the network reachability needed for the approved purpose.

### Logging and monitoring

Authentication events, privileged activity, firewall activity, endpoint events, and administrative actions must be logged when technically feasible. Required log sources must be reviewed through the SIEM or another documented monitoring process.

### Backup and restore validation

Backups must be monitored and restore procedures must be tested on a scheduled basis. Restore test results must be documented and retained as evidence.

## Exceptions

Exceptions must include:

- business justification
- affected requirement
- System Owner approval
- compensating control, when applicable
- review date
- expiration date, when applicable

An exception that requires formal acceptance of system-level residual risk must be elevated to the Authorizing Official.

## Evidence

Evidence may include user access reports, role matrices, access approval records, privileged access reports, MFA configuration evidence, firewall and VPN rules, network diagrams, SIEM log source lists, alert examples, backup logs, restore test reports, and change approval records.

## Compliance and review

The SSO tracks findings, remediation, and evidence status. The System Owner remains accountable for the system-level risks and treatment decisions. Where assessment or retesting is required, the Control Assessor reviews the evidence and documents the assessment conclusion.

This policy should be reviewed annually or after major changes to identity systems, network architecture, remote access methods, logging coverage, or backup and recovery processes.
