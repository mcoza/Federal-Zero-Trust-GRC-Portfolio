# 00A - System Context

## Why this view exists

The five risks make more sense when the environment is visible as one connected system instead of a list of controls.

This is a logical context view for the scenario. It shows the trust boundaries and system relationships that matter to the five risks. It is not a device-level network topology.

## Environment view

```text
                         +----------------------+
                         |     Remote Users     |
                         +----------+-----------+
                                    |
                                    v
                         +----------------------+
                         | Remote Access / VPN  |
                         +----------+-----------+
                                    |
                                    v
+----------------+       +----------------------+       +----------------+
| Internal Users | ----> |      User Zone       | ----> | Business Apps  |
+----------------+       +----------+-----------+       +--------+-------+
                                   |                             |
                                   |                             v
                                   |                    +----------------+
                                   +------------------> | App Servers    |
                                                        +--------+-------+
                                                                 |
                                                                 v
                                                        +----------------+
                                                        | File / Data    |
                                                        | Resources      |
                                                        +----------------+

+----------------------+          privileged management paths
| Privileged Admins    | ----------------------------------------------+
+----------+-----------+                                               |
           |                                                           v
           v                                                  +----------------+
+----------------------+                                      | Internal       |
| Administrative Zone  | -----------------------------------> | Systems        |
+----------------------+                                      +----------------+

Critical systems and security devices
            |
            +---------------------> +----------------------+
                                    | SIEM / Logging       |
                                    +----------------------+

Critical systems and data
            |
            +---------------------> +----------------------+
                                    | Backup / Recovery    |
                                    +----------------------+

External-facing services
            |
            +---------------------> +----------------------+
                                    | DMZ                  |
                                    +----------------------+
```

## Where the risks sit

| Risk | Main area in the context view | What can go wrong |
|---|---|---|
| R-001 Excessive user access | Users, business applications, file/data resources | A user can reach or change more than the approved role requires |
| R-002 Privileged access governance | Privileged admins and administrative paths | Excessive or poorly governed admin access increases the impact of misuse or compromise |
| R-003 Insufficient network segmentation | User, admin, remote access, server, and DMZ boundaries | A compromised account or endpoint can move into systems that should be isolated |
| R-004 Incomplete SIEM/logging coverage | SIEM and the systems that should send it security events | Important activity may not be available for detection or investigation |
| R-005 Unvalidated backup and restore | Backup/recovery systems and protected data | Backups may exist without enough evidence that selected data can actually be restored |

## Zero Trust connection

The context view also shows why the Zero Trust references are relevant without requiring a separate maturity model:

- **Identity:** user and privileged access decisions
- **Networks:** segmentation, approved traffic paths, and remote access
- **Visibility and Analytics:** logs reaching the SIEM and being reviewed
- **Governance:** risk ownership, policy, evidence, remediation, and validation

The [Project Overview](00-project-overview.md) explains the scenario and frameworks. The [Risk Register](02-risk-register.csv) contains the five risk statements and treatments.
