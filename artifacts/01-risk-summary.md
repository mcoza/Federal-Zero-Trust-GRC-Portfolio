# 01 - Risk Summary

## Summary

The biggest concerns in this environment are access, privileged accounts, network segmentation, logging coverage, and backup recovery.

The three highest-ranked risks are excessive user access, weak privileged access governance, and insufficient network segmentation. All three can make a compromise more damaging by giving an attacker or misused account more access than it should have.

The scores below are the initial risk scores for the scenario. I have not assigned residual risk because the remaining risk areas still need evidence showing that the relevant controls are in place and working.

## Priority view

| Risk | Initial score | Rating | Why it matters | Next action | Owner |
|---|---:|---|---|---|---|
| R-001 Excessive user access | 20 | High | Users may have access they do not need | Continue access reviews and remove unsupported permissions | IAM Team |
| R-002 Privileged access governance | 20 | High | Weak admin controls can make misuse or account compromise much more damaging | Review privileged accounts, require MFA, and separate admin access from standard use | Security / IAM Team |
| R-003 Insufficient network segmentation | 20 | High | A compromised endpoint may be able to reach systems that should be isolated | Define network zones and restrict inter-zone traffic to approved paths | Network Team |
| R-004 Incomplete SIEM/logging coverage | 15 | High | Missing events can delay detection and investigation | Onboard critical authentication, firewall, endpoint, and administrative logs | SOC Team |
| R-005 Unvalidated backup and restore | 12 | Moderate | Backups are less useful if nobody has proven they can be restored | Perform and document restore testing | SysAdmin Team |

## Completed assessment

I completed one access-control review using 12 fictional user records. Ten accounts stayed within their approved access and two could do things their roles did not allow.

One Finance Analyst could edit payroll records. One Support Analyst could administer servers.

Those two exceptions were tracked in POAM-001, corrected, and retested. Both accounts passed the retest, so POAM-001 is closed.

R-001 stays open because fixing two accounts does not prove the larger access-review process is consistently effective across the environment.

## Recommended next actions

1. Keep scheduled access reviews in place and retain the evidence for R-001.
2. Review privileged-account ownership, separation, MFA, and activity monitoring for R-002.
3. Document the approved network zones and remote-access paths, then compare the actual firewall and ACL rules against them.
4. Confirm that required log sources are actively sending events to the SIEM and that the data is being reviewed.
5. Run a documented restore test and keep the results.

## What I would look at next

The open risks need evidence, not just planned fixes. The next useful step would be targeted testing of the highest-priority open controls so the risk picture can be updated with something stronger than assumptions.
