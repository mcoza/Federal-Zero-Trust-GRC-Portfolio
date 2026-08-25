# 05 - Security Control Policy

## Document control

| Field | Value |
|---|---|
| Document | Security Control Policy |
| Project | Federal Zero Trust GRC Portfolio |
| Author | Mark C. |
| Version | 1.0 |
| Modeled Policy Owner | Security / GRC Team |
| Modeled Approval Authority | System Owner |
| Effective Date | 2026-08-25 |
| Review Cycle | Annual or after major system change |

## Purpose

This policy defines security requirements for the modeled environment in the areas covered by the portfolio: user access, privileged access, network segmentation, remote access, logging and monitoring, backup validation, and exceptions.

It is intentionally broader than a single access-control policy because the portfolio risks span several control areas.

## Scope

This policy applies to the modeled federal enterprise environment, including internal users, privileged users, remote access users, application servers, file shares, administrative systems, network infrastructure, SIEM/logging systems, backup systems, and DMZ systems.

## Roles and responsibilities

| Role / Team | Responsibility |
|---|---|
| System Owner | Approves business requirements and risk decisions for the modeled system |
| IAM Team | Manages user access, access reviews, and account changes |
| Security / IAM Team | Manages privileged-access requirements and privileged MFA |
| Network Team | Manages segmentation, firewall/ACL rules, and approved remote-access paths |
| SOC Team | Manages required security logging, monitoring, and review activity |
| SysAdmin Team | Manages backup jobs and restore testing |
| Security / GRC Team | Tracks policy exceptions, findings, remediation, and evidence status |

## Policy requirements

### Role-based access

Access to systems and data must be based on documented job-role requirements. Users must be granted only the access needed for approved business functions.

### Access reviews

User and privileged access must be reviewed on a scheduled basis and after significant role changes. Access that is no longer required must be removed or modified.

### Privileged access

Privileged accounts must be separated from standard user accounts where applicable. Privileged access must require multi-factor authentication and should be monitored through available logging and SIEM capabilities.

### Network segmentation

The internal network must be separated into defined zones where applicable, including user, server, administrative, remote access, DMZ, logging, and backup zones.

### Inter-zone traffic

Traffic between network zones must be denied by default and allowed only when there is a documented business requirement, an approved owner, and an associated logging requirement where feasible.

### Remote access

Remote access must use approved authentication methods, be limited to authorized users, and provide only the network reachability needed for the approved purpose.

### Logging and monitoring

Authentication events, privileged activity, firewall activity, endpoint events, and administrative actions must be logged when technically feasible. Required log sources must be reviewed through the SIEM or another documented monitoring process.

### Backup and restore validation

Backups must be monitored and restore procedures must be tested on a scheduled basis. Restore-test results must be documented and retained as evidence.

## Exceptions

Exceptions must include:

- business justification
- affected requirement
- risk owner or system owner approval
- compensating control, when applicable
- review date
- expiration date, when applicable

## Evidence

Evidence may include access-review exports, RBAC matrices, privileged-group exports, MFA configuration evidence, firewall and VPN rules, network diagrams, SIEM log-source lists, alert examples, backup logs, restore-test reports, and change-approval records.

## Compliance and review

Findings against this policy should be tracked through the portfolio's remediation process. Closure requires evidence that the corrective action was completed and, where appropriate, retested or validated.

This modeled policy should be reviewed annually or after major changes to identity systems, network architecture, remote-access methods, logging coverage, or backup/recovery processes.
