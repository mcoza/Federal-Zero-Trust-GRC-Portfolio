# 01 - Risk Summary

## What drives the risk picture

The five risks are ranked by likelihood and impact using the project scoring model. The three highest-ranked risks are excessive user access, weak privileged access governance, and insufficient network segmentation because each can expand what an attacker or misused account can reach or change.

R-004 is also High because missing logs can delay detection and investigation across important systems. R-005 is Moderate because failed recovery can cause serious disruption, but its expected impact is narrower than the access and segmentation risks in this scenario.

I have not assigned residual risk. Most of the open conditions still need evidence that the relevant controls are implemented and working consistently.

## What the completed assessment tells me

The R-001 access review tested all 12 accounts in the available population against their approved role access.

Ten accounts stayed within the approved baseline. Two did not:

- U-005, Finance Analyst, could edit payroll records
- U-009, Support Analyst, could administer servers

Those two exceptions were tracked under POAM-001, corrected, and retested successfully. The testing procedure and account-level results are documented in the [Access Review Workpaper](07B-access-review-workpaper.md).

That changes what I know about the specific exceptions, but not enough to close R-001. One corrected review does not establish that the broader access-review process is consistently effective across the environment.

## What still needs evidence

| Risk | Evidence question that still matters |
|---|---|
| R-001 | Do repeated access reviews show that unnecessary access is identified and removed consistently? |
| R-002 | Are privileged accounts approved, separated from standard use, protected with MFA, and monitored? |
| R-003 | Do deployed firewall, ACL, VPN, and segmentation rules match approved network paths? |
| R-004 | Are required security log sources reaching the SIEM and being reviewed? |
| R-005 | Can selected backups actually be restored and validated? |

The next useful work is targeted testing of those open conditions. The current management position is summarized in the [Executive Risk View](01A-executive-risk-view.md).
