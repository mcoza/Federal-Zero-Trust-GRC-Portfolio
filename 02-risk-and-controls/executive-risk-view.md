# Executive Risk View

This is the management-facing view of current risk status, ownership, remediation position, and next decisions. Detailed assessment reasoning is kept in the [Analyst Risk Summary](risk-summary.md).

## Current position

- **Tracked risks:** 5
- **High:** 4
- **Moderate:** 1
- **POA&M items:** 5
- **Closed:** 1
- **Open:** 4

POAM-001 is closed after both access exceptions under R-001 were corrected and passed retest. R-001 remains open because the broader access-review process still needs additional evidence.

The other four POA&M items are scenario baseline conditions, not completed control-assessment findings.

## Risk heatmap

| Impact \ Likelihood | 1 Rare | 2 Unlikely | 3 Possible | 4 Likely | 5 Almost Certain |
|---|---|---|---|---|---|
| **5 Severe** |  |  | R-004 | R-001, R-002, R-003 |  |
| **4 Major** |  |  | R-005 |  |  |
| **3 Moderate** |  |  |  |  |  |
| **2 Minor** |  |  |  |  |  |
| **1 Minimal** |  |  |  |  |  |

## Priority status

| Risk | Rating | Risk Action Owner | Management position |
|---|---|---|---|
| R-001 Excessive user access | High | IAM Team | POAM-001 closed; broader risk remains open pending repeated review evidence |
| R-002 Privileged access governance | High | Security / IAM Team | Prioritize testing of approval, separation, MFA, and monitoring |
| R-003 Insufficient network segmentation | High | Network Team | Validate approved zones and traffic paths against deployed rules |
| R-004 Incomplete SIEM/logging coverage | High | SOC Team | Validate critical log-source coverage and review activity |
| R-005 Unvalidated backup and restore | Moderate | SysAdmin Team | Complete and document a restore test |

## Management priorities

1. Establish repeated access-review evidence for R-001.
2. Test privileged-access and segmentation controls.
3. Validate SIEM coverage and review activity.
4. Complete and document a restore test.

All five risks remain in mitigation status. No formal system-level risk acceptance or authorization decision is documented in this scenario.