# 01 - Executive Risk Summary

## Document control

| Field | Value |
|---|---|
| Document | Executive Risk Summary |
| Project | Federal Zero Trust GRC Portfolio |
| Author | Mark C. |
| Version | 1.5 |

## Summary

The environment has elevated risk around user access, privileged access, network segmentation, logging coverage, and backup validation.

The highest initial risk scores are excessive user access, weak privileged access governance, and insufficient segmentation. These issues could make a compromised account or endpoint more damaging by allowing unnecessary access, administrative misuse, or lateral movement.

The scores reflect the scenario conditions before the recommended treatment actions are completed and validated. Residual risk has not been calculated across the environment because the relevant controls have not been validated across the full scope.

## Priority view

| Risk | Initial score | Rating | Why it matters | Immediate action | Action owner |
|---|---:|---|---|---|---|
| R-001 Excessive user access | 20 | High | Users may retain access beyond their role, increasing unauthorized access risk | Continue scheduled access reviews and remove unsupported permissions when identified | IAM Team |
| R-002 Privileged access governance | 20 | High | Weak privileged access governance can increase the impact of misuse or account compromise | Review privileged accounts, enforce MFA, and separate admin access from standard use | Security / IAM Team |
| R-003 Insufficient network segmentation | 20 | High | A compromised endpoint could reach systems that should be isolated | Define zones and restrict inter-zone traffic to approved paths | Network Team |
| R-004 Incomplete SIEM/logging coverage | 15 | High | Missing events can delay detection and investigation | Onboard critical authentication, firewall, endpoint, and administrative logs | SOC Team |
| R-005 Unvalidated backup and restore | 12 | Moderate | Recovery may fail when needed if restore testing has not been proven | Perform and document scheduled restore testing | SysAdmin Team |

## Completed assessment result

One scoped access-control assessment identified two unsupported group memberships in a 12-record synthetic dataset. The exceptions were tracked through POAM-001, corrected in updated evidence, retested, and closed.

That closure resolves the two identified exceptions. R-001 remains open because the broader access-governance condition requires continued review and evidence beyond one completed finding.

## Recommended actions

1. Continue scheduled access reviews and retain evidence for R-001.
2. Review privileged account lifecycle, separation, MFA, and activity monitoring for R-002.
3. Define approved network zones and remote access paths before validating firewall and ACL evidence.
4. Confirm required log sources are actively ingesting into the SIEM and that review evidence exists.
5. Perform a documented restore test and retain the result as evidence.

## What leadership would need next

For the remaining open risks, leadership would need stronger evidence that the planned controls are implemented and working before making broader risk acceptance or residual risk decisions. The next useful outputs would be targeted control tests and validation evidence for the highest-priority open risks.
