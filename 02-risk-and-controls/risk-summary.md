# Analyst Risk Summary

This file explains the reasoning behind the risk picture: why the risks are ranked as they are, what the completed assessment actually supports, and what evidence is still missing. For the current management status, ownership, and priorities, see the [Executive Risk View](executive-risk-view.md).

## Why the risks rank where they do

The five risks are ranked by likelihood and impact using the project scoring model. The three highest-ranked risks are excessive user access, weak privileged access governance, and insufficient network segmentation because each can expand what an attacker or misused account can reach or change.

R-004 is also High because missing logs can delay detection and investigation across important systems. R-005 is Moderate because failed recovery can cause serious disruption, but its expected impact is narrower than the access and segmentation risks in this scenario.

I have not assigned residual risk. Most of the open conditions still need evidence that the relevant controls are implemented and working consistently.

## What the completed assessment supports

The R-001 access review tested all 12 accounts in the available population against their approved role access.

Ten accounts stayed within the approved baseline. Two did not:

- U-005, Finance Analyst, could edit payroll records
- U-009, Support Analyst, could administer servers

Those two exceptions were tracked under POAM-001, corrected, and retested successfully. The testing procedure and account-level results are documented in the [Access Review Workpaper](../03-assessment-and-evidence/access-review-workpaper.md).

The retest supports closure of those two exceptions and POAM-001. It does not support closing R-001 because one corrected review does not establish that the broader access-review process is consistently effective across the environment.

## What remains unproven

| Risk | Evidence question that still matters |
|---|---|
| R-001 | Do repeated access reviews show that unnecessary access is identified and removed consistently? |
| R-002 | Are privileged accounts approved, separated from standard use, protected with MFA, and monitored? |
| R-003 | Do deployed firewall, ACL, VPN, and segmentation rules match approved network paths? |
| R-004 | Are required security log sources reaching the SIEM and being reviewed? |
| R-005 | Can selected backups actually be restored and validated? |

The next useful analyst work is targeted testing of those open conditions. I would not rescore residual risk until evidence shows how the implemented controls change the underlying condition.