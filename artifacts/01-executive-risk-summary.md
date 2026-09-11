# 01 - Executive Risk Summary

## Document control

| Field | Value |
|---|---|
| Document | Executive Risk Summary |
| Project | Federal Zero Trust GRC Portfolio |
| Author | Mark C. |
| Version | 1.4 |

## Summary

The environment has elevated risk around user access, privileged access, network segmentation, logging coverage, and backup validation.

The highest inherent risk scores are excessive user access, weak privileged access governance, and insufficient segmentation. These issues could make a compromised account or endpoint more damaging by allowing unnecessary access, administrative misuse, or lateral movement.

The scores are inherent risk estimates based on the conditions in the scenario. I have not calculated residual risk across the environment because the controls have not been validated across the full scope. Closing one scoped finding does not establish the residual risk of the broader environment.

## Priority view

| Risk | Inherent score | Rating | Why it matters | Immediate action | Action owner |
|---|---:|---|---|---|---|
| R-001 Excessive user access | 20 | High | Users may retain access beyond their role, increasing unauthorized access risk | Continue scheduled access reviews and remove unsupported permissions when identified | IAM Team |
| R-002 Weak privileged access separation | 20 | High | Privileged compromise could affect multiple systems and security settings | Review privileged accounts, enforce MFA, and separate admin access from standard use | Security / IAM Team |
| R-003 Insufficient network segmentation | 20 | High | A compromised endpoint could reach systems that should be isolated | Define zones and restrict inter-zone traffic to approved paths | Network Team |
| R-004 Incomplete SIEM/logging coverage | 15 | High | Missing events can delay detection and investigation | Onboard critical authentication, firewall, endpoint, and administrative logs | SOC Team |
| R-005 Unvalidated backup and restore | 12 | Moderate | Recovery may fail when needed if restore testing has not been proven | Perform and document scheduled restore testing | SysAdmin Team |

## Access review and remediation result

For R-001, I used 12 synthetic user records to test whether access matched the approved role. Ten records matched and two contained unsupported group memberships.

The initial scoped AC-6 assessment result was **Other Than Satisfied** because the expected condition was not met across the full set of records.

The two exceptions were tracked in POAM-001. Updated synthetic evidence shows that Payroll-Write was removed from U-005 and Server-Admins was removed from U-009. Both affected accounts passed the scoped remediation retest, and POAM-001 is closed for this portfolio exercise.

The retest validates remediation of those two exceptions only. It does not establish that every AC-6 determination or every access control in the fictional environment is effective.

## Recommended actions

1. Continue scheduled access reviews and retain evidence for R-001.
2. Review privileged account lifecycle, separation, MFA, and activity monitoring for R-002.
3. Define approved network zones and remote access paths before validating firewall and ACL evidence.
4. Confirm required log sources are actively ingesting into the SIEM and that review evidence exists.
5. Perform a documented restore test and retain the result as evidence.

## What leadership would need next

For the remaining open risks, leadership would need stronger evidence that the planned controls are implemented and working before making broader risk acceptance or residual risk decisions. The next useful outputs would be targeted control tests and validation evidence for the highest-priority open risks.
