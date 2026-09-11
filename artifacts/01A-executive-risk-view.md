# 01A - Executive Risk View

## Current position

- **Tracked risks:** 5
- **High:** 4
- **Moderate:** 1
- **POA&M items:** 5
- **Closed:** 1
- **Open:** 4

One scoped access-control assessment identified two exceptions under R-001. Both were corrected and passed retest, so POAM-001 is closed. R-001 remains open because the broader access-review process still needs enough evidence to support a wider conclusion.

The remaining four POA&M items come from scenario baseline conditions and have not been presented as completed control assessments.

## Risk heatmap

| Impact \ Likelihood | 1 Rare | 2 Unlikely | 3 Possible | 4 Likely | 5 Almost Certain |
|---|---|---|---|---|---|
| **5 Severe** |  |  | R-004 | R-001, R-002, R-003 |  |
| **4 Major** |  |  | R-005 |  |  |
| **3 Moderate** |  |  |  |  |  |
| **2 Minor** |  |  |  |  |  |
| **1 Minimal** |  |  |  |  |  |

## Priority status

| Risk | Rating | Risk Action Owner | Current position |
|---|---|---|---|
| R-001 Excessive user access | High | IAM Team | Two exceptions were corrected and retested; broader risk remains open |
| R-002 Privileged access governance | High | Security / IAM Team | Evidence still needed for account review, separation, MFA, and monitoring |
| R-003 Insufficient network segmentation | High | Network Team | Approved zones and traffic paths still need to be validated against deployed rules |
| R-004 Incomplete SIEM/logging coverage | High | SOC Team | Critical log-source coverage and review still need validation |
| R-005 Unvalidated backup and restore | Moderate | SysAdmin Team | A documented restore test is still needed |

## Management attention

1. Build repeated access-review evidence for R-001.
2. Test privileged-access and segmentation controls next.
3. Validate SIEM coverage and review activity.
4. Complete and document a restore test.

All five risks remain in mitigation status. No formal system-level risk acceptance or authorization decision is documented in this scenario.
