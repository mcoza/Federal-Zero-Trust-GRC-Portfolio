# 01 - Executive Risk Summary

## Document control

| Field | Value |
|---|---|
| Document | Executive Risk Summary |
| Project | Federal Zero Trust GRC Portfolio |
| Author | Mark C. |
| Version | 1.3 |

## Summary

The environment has elevated risk around user access, privileged access, network segmentation, logging coverage, and backup validation.

The highest inherent risk scores are excessive user access, weak privileged access governance, and insufficient segmentation. These issues could make a compromised account or endpoint more damaging by allowing unnecessary access, administrative misuse, or lateral movement.

The scores are inherent risk estimates based on the conditions in the scenario. I have not calculated residual risk because the controls and remediation have not been fully validated.

## Priority view

| Risk | Inherent score | Rating | Why it matters | Immediate action | Action owner |
|---|---:|---|---|---|---|
| R-001 Excessive user access | 20 | High | Users may retain access beyond their role, increasing unauthorized access risk | Review access against approved roles and remove unsupported permissions | IAM Team |
| R-002 Weak privileged access separation | 20 | High | Privileged compromise could affect multiple systems and security settings | Review privileged accounts, enforce MFA, and separate admin access from standard use | Security / IAM Team |
| R-003 Insufficient network segmentation | 20 | High | A compromised endpoint could reach systems that should be isolated | Define zones and restrict inter-zone traffic to approved paths | Network Team |
| R-004 Incomplete SIEM/logging coverage | 15 | High | Missing events can delay detection and investigation | Onboard critical authentication, firewall, endpoint, and administrative logs | SOC Team |
| R-005 Unvalidated backup and restore | 12 | Moderate | Recovery may fail when needed if restore testing has not been proven | Perform and document scheduled restore testing | SysAdmin Team |

## Access review result

For R-001, I used 12 synthetic user records to test whether access matched the approved role. Ten records matched and two contained unsupported group memberships.

The AC-6 Least Privilege result is **Other Than Satisfied** because the expected condition was not met across the full set of records.

The two exceptions are tracked in POAM-001 for correction and retesting.

## Recommended actions

1. Correct the two access exceptions and retest the affected accounts.
2. Review privileged account lifecycle, separation, MFA, and activity monitoring for R-002.
3. Define approved network zones and remote access paths before validating firewall and ACL evidence.
4. Confirm required log sources are actively ingesting into the SIEM and that review evidence exists.
5. Perform a documented restore test and retain the result as evidence.

## What leadership would need next

Before making a risk acceptance or residual risk decision, the organization would need stronger evidence that the planned controls are implemented and working. The next useful outputs would be completed remediation evidence, targeted control tests, and retest results for the highest priority risks.