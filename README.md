# Federal Zero Trust GRC Portfolio

**IT Risk Assessment, Control Testing, Evidence Review, and Remediation**

This repo started as my graduate cybersecurity capstone. I rebuilt it around a fictional civilian federal environment so I could work through the GRC side of real security problems.

I use the scenario to write and prioritize risks, assign ownership, choose controls that fit, decide what evidence matters, document findings, and follow remediation through validation.

NIST SP 800-53 Rev. 5 is the main control framework. NIST SP 800-37, NIST SP 800-53A, NIST SP 1308, NIST SP 800-207, and the CISA Zero Trust Maturity Model provide supporting risk, assessment, governance, and Zero Trust context.

## What is in the repo

The project covers five risk areas:

- excessive user access
- privileged access governance
- network segmentation and remote access
- SIEM and logging coverage
- backup and restore validation

Across those areas, the repo includes risk scoring, system context, control mapping, evidence planning, policy, responsibility assignment, remediation tracking, executive reporting, and one access-control review carried through workpaper testing, retesting, and closure.

## Evidence and authorship

I authored the risk analysis, control mapping, test procedure, workpaper, and remediation narrative as a portfolio exercise. The account data and retest records are synthetic scenario inputs, not exports from a federal system. The team and assessor titles describe scenario responsibilities; they do not represent separate people who performed or approved this work.

The completed example demonstrates evidence comparison, exception documentation, and a scoped closure decision. It does not establish production control effectiveness, independent assessment, or federal authorization.

## Current snapshot

- **Risks:** 5
- **High initial risks:** 4 (scenario ratings; residual risk not assessed)
- **POA&M items:** 5 (1 closed, 4 open)
- **Evidence requirements:** 8 (an evidence request plan, not 8 collected artifacts)
- **Completed control assessments:** 1 scoped AC-6 exercise (12 accounts; 10 pass, 2 exceptions)
- **Assessment workpapers:** 1
- **Completed remediation retests:** 1

## 5-minute reviewer path

Follow one example from decision to source records:

| Step | Open | What to verify |
|---|---|---|
| 1. Management decision | [Executive Risk View](02-risk-and-controls/executive-risk-view.md) | Five risks remain open; initial ratings have not been rescored after remediation |
| 2. Risk and ownership | [Risk Register](02-risk-and-controls/risk-register.csv) — R-001 | Score 20 / High; System Owner owns the risk; IAM Team carries out treatment |
| 3. Test and source | [Workpaper WP-AC6-001](03-assessment-and-evidence/access-review-workpaper.md) → [12-account dataset](03-assessment-and-evidence/access-review.csv) | Compare approved and observed access; U-005 and U-009 have extra permissions |
| 4. Corrective action | [Remediation Tracker](04-remediation-and-validation/remediation-tracker.csv) — POAM-001 | A-01 and A-02 share one IAM-owned corrective action with explicit closure requirements |
| 5. Retest and decision | [Remediation Validation](04-remediation-and-validation/remediation-validation.md) → [two-account retest](04-remediation-and-validation/access-retest.csv) | Both corrected rows match the original baseline; scoped closure leaves R-001 open |

For the ranking rationale and remaining evidence questions, see the [Analyst Risk Summary](02-risk-and-controls/risk-summary.md). For the distinction between risk accountability, remediation, and assessment, see the [Responsibility Matrix](01-context-and-governance/responsibility-matrix.md).

## Explore the project

### [01 - Context and Governance](01-context-and-governance/)

Understand the scenario, system relationships, policy, and who is accountable for the work.

- [Project Overview](01-context-and-governance/project-overview.md)
- [System Context](01-context-and-governance/system-context.md)
- [Security Policy](01-context-and-governance/security-policy.md)
- [Responsibility Matrix](01-context-and-governance/responsibility-matrix.md)

### [02 - Risk and Controls](02-risk-and-controls/)

See how the five risks are prioritized, scored, assigned, and connected to NIST controls.

- [Analyst Risk Summary](02-risk-and-controls/risk-summary.md)
- [Executive Risk View](02-risk-and-controls/executive-risk-view.md)
- [Risk Register](02-risk-and-controls/risk-register.csv)
- [Risk Scoring](02-risk-and-controls/risk-scoring.md)
- [Control Mapping](02-risk-and-controls/control-mapping.csv)
- [Control Mapping Notes](02-risk-and-controls/control-mapping-notes.md)

### [03 - Assessment and Evidence](03-assessment-and-evidence/)

Follow the evidence plan and the completed AC-6 access review from source data through account-level testing and conclusion.

- [Evidence Review](03-assessment-and-evidence/evidence-review.csv)
- [Access Review Data](03-assessment-and-evidence/access-review.csv)
- [Access Control Review](03-assessment-and-evidence/access-control-review.md)
- [Access Review Workpaper](03-assessment-and-evidence/access-review-workpaper.md)

### [04 - Remediation and Validation](04-remediation-and-validation/)

See how issues are tracked, corrected, retested, and closed without automatically closing the broader risk.

- [Remediation Process](04-remediation-and-validation/remediation-process.md)
- [Remediation Tracker](04-remediation-and-validation/remediation-tracker.csv)
- [Access Retest](04-remediation-and-validation/access-retest.csv)
- [Remediation Validation](04-remediation-and-validation/remediation-validation.md)

## How the pieces fit together

Risk and owner → control and evidence → test and finding → corrective action and owner → retest and scoped closure → risk reporting.

A closed finding does not automatically close the larger risk. The risk stays open until there is enough evidence to support that decision.
