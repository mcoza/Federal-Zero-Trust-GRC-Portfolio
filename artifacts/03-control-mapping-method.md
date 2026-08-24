# 03A — Control Mapping Method

## Purpose

This matrix maps identified portfolio risks to selected NIST SP 800-53 Rev. 5 control areas. Control mappings are based on the risk condition, affected asset area, recommended treatment, and evidence needed to validate implementation.

## Mapping logic

| Step | Action | Example |
|---:|---|---|
| 1 | Identify risk condition | Excessive user access |
| 2 | Select relevant control family | AC — Access Control |
| 3 | Select control ID | AC-6 Least Privilege |
| 4 | Define implementation expectation | User permissions are limited by documented role requirements |
| 5 | Identify evidence needed | RBAC matrix, group membership export, access review notes |

## Control type definitions

| Control type | Description | Examples |
|---|---|---|
| Management / Administrative | Policy, governance, planning, review, ownership, and risk decision controls. | Policies, access reviews, POA&M tracking, risk acceptance |
| Technical | System-enforced controls configured or performed through technology. | MFA, firewall rules, logging configuration, segmentation, access restrictions |
| Operational | Recurring human or process-driven security activities. | Log review, backup testing, access review execution, evidence collection |
