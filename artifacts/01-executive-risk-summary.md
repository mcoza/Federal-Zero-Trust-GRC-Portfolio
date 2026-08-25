# 01 - Executive Risk Summary

## Document control

| Field | Value |
|---|---|
| Document | Executive Risk Summary |
| Project | Federal Zero Trust GRC Portfolio |
| Author | Mark C. |
| Version | 1.1 |

## Summary

The modeled environment has elevated unauthorized-access risk across user access, privileged access, network segmentation, logging coverage, and backup validation.

The highest inherent risk scores are tied to excessive user access, weak privileged access governance, and insufficient segmentation. These conditions can increase the impact of a compromised account or endpoint by allowing unnecessary access, administrative misuse, or lateral movement.

The scores in this portfolio are inherent-risk estimates based on the modeled conditions. Residual risk is not calculated yet because control effectiveness and remediation have not been validated across the full environment.

## Priority view

| Risk | Inherent score | Rating | Why it matters | Immediate action | Action owner |
|---|---:|---|---|---|---|
| R-001 Excessive user access | 20 | High | Users may retain access beyond their role, increasing unauthorized access risk | Review access against approved roles and remove unsupported permissions | IAM Team |
| R-002 Weak privileged access separation | 20 | High | Privileged compromise could affect multiple systems and security settings | Separate admin accounts, enforce privileged MFA, and review privileged groups | Security / IAM Team |
| R-003 Insufficient network segmentation | 20 | High | A compromised endpoint could reach systems that should be isolated | Define zones and restrict inter-zone traffic to approved paths | Network Team |
| R-004 Incomplete SIEM/logging coverage | 15 | High | Missing events can delay detection and investigation | Onboard critical authentication, firewall, endpoint, and administrative logs | SOC Team |
| R-005 Unvalidated backup and restore | 12 | Moderate | Recovery may fail when needed if restore testing is not proven | Perform and document scheduled restore testing | SysAdmin Team |

## Assessment result already modeled

A small modeled access review was performed for R-001 using 12 synthetic user records. Ten records matched the approved role-based access expectation and two contained unsupported group memberships.

That result supports a finding that the access-review / least-privilege control objective is not operating consistently across the modeled population. The exceptions are traced to POAM-001 for remediation and later retesting.

## Recommended actions

1. Correct the two modeled access exceptions and retest the affected accounts.
2. Review privileged accounts and privileged MFA requirements using AC-6 and IA-2(1) as part of the control plan.
3. Define approved network zones and remote-access paths before validating firewall and ACL evidence.
4. Confirm required log sources are actively ingesting into the SIEM and that review evidence exists.
5. Perform a documented restore test and retain the result as evidence.

## What leadership would need next

Before making a risk-acceptance or residual-risk decision, the modeled organization would need stronger evidence that the planned controls are implemented and operating as intended. The next useful outputs are completed remediation evidence, targeted control tests, and retest results for the highest-priority risks.
