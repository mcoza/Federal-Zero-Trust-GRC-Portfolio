# 01A - Executive Risk View

## Current position

The environment has five tracked risks. Four are rated High and one is Moderate using the project scoring model.

One scoped access-control assessment has been completed. It identified two exceptions under R-001. Both were remediated and passed retest, so POAM-001 is closed. The broader R-001 risk remains open because one corrected review does not establish that access governance is consistently effective across the environment.

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

| Risk | Rating | Status | Risk Action Owner | Current position | Next action |
|---|---|---|---|---|---|
| R-001 Excessive user access | High | Open | IAM Team | One 12-account review found two exceptions. Both were corrected and retested successfully. | Continue scheduled access reviews and retain evidence across a broader period |
| R-002 Privileged access governance | High | Open | Security / IAM Team | Baseline condition identifies weaknesses in admin separation, review, MFA, and monitoring | Review privileged accounts, MFA, separation, and monitoring evidence |
| R-003 Insufficient network segmentation | High | Open | Network Team | Baseline condition identifies incomplete documentation and restriction of network paths | Document zones and approved flows, then compare deployed rules with the approved design |
| R-004 Incomplete SIEM/logging coverage | High | Open | SOC Team | Baseline condition identifies missing critical log sources | Confirm required sources, onboard gaps, and validate ingestion and review |
| R-005 Unvalidated backup and restore | Moderate | Open | SysAdmin Team | Baseline condition identifies insufficient restore-test evidence | Perform and document a selected restore test |

## Remediation position

- **POA&M items:** 5
- **Closed:** 1
- **Open:** 4
- **Closed item:** POAM-001 for the two R-001 access exceptions
- **Open items:** POAM-002 through POAM-005

Open POA&M items have closure requirements defined, but their closure-evidence fields remain blank until evidence is produced and validated.

## Management attention

The immediate focus is evidence, not additional risk statements.

1. Build enough repeated access-review evidence to make a broader judgment about R-001.
2. Test the highest-priority privileged-access and segmentation conditions instead of leaving them at baseline assumptions.
3. Validate that critical security logs are reaching the SIEM and are actually being reviewed.
4. Produce a documented restore result for R-005.

## Decisions and escalation

All five risks remain in mitigation status in the current scenario. No formal system-level risk acceptance or authorization decision is documented here.

The System Owner remains accountable for the five system-level risks. A formal authorization or system-level risk acceptance decision would be handled by the Authorizing Official under the governance model in the [Responsibility Matrix](05A-responsibility-matrix.md).
