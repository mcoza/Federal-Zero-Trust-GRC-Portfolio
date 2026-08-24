# 05 — Access Control & Network Segmentation Policy

## Document control

| Field | Value |
|---|---|
| Document | Access Control and Network Segmentation Policy |
| Project | Federal Zero Trust GRC Portfolio |
| Author | Mark C. |
| Version | 1.0 |

## Purpose

The purpose of this policy is to reduce unauthorized access and lateral movement risk by defining requirements for access governance, privileged access separation, network segmentation, remote access control, logging, and backup validation.

## Scope

This policy applies to the modeled federal enterprise environment, including internal users, privileged users, remote access users, application servers, file shares, administrative systems, network infrastructure, SIEM/logging systems, backup systems, and DMZ system.

## Policy statements

### Role-Based Access Control

Access to systems and data must be based on documented job role requirements. Users must be granted only the access necessary to perform approved business functions.

### Access Reviews

User access and privileged access must be reviewed on a scheduled basis. Access that is no longer required must be removed or modified.

### Privileged Access

Privileged accounts must be separated from standard user accounts. Administrative access must require strong authentication and should be monitored through available logging and SIEM capabilities.

### Network Segmentation

The internal network must be separated into defined zones, including user, server, administrative, remote access, DMZ, logging, and backup zones where applicable.

### Inter-Zone Traffic

Traffic between network zones must be denied by default and allowed only when there is a documented business requirement, an approved system owner, and an associated logging requirement.

### Remote Access

Remote access must use approved authentication methods and must not provide broad internal network reachability unless required and documented.

### Logging and Monitoring

Authentication events, privileged access activity, firewall activity, endpoint events, and administrative actions must be logged when technically feasible and reviewed in a SIEM or other monitoring processes.

### Backup and Restore Validation

Backup and restore processes must be tested on a scheduled basis. Restore test results must be documented and retained as evidence.

## Exceptions

Exceptions to this policy must include a business justification, risk owner approval, a compensating control, a review date, and an expiration date, when applicable.

## Evidence requirements

Evidence may include access review exports, RBAC matrices, privileged group exports, MFA configuration evidence, firewall rules, network diagrams, SIEM log source lists, alert examples, backup logs, restore test reports, and change approval records.

## Review cycle

This policy should be reviewed annually or after major changes to identity systems, network architecture, remote access methods, SIEM/logging coverage, or backup/recovery processes.
