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

## Current snapshot

- **Risks:** 5
- **High initial risks:** 4
- **POA&M items:** 5 (1 closed, 4 open)
- **Evidence requirements:** 8
- **Completed control assessments:** 1
- **Assessment workpapers:** 1
- **Completed remediation retests:** 1

## Start here

For a quick review of the project:

1. [Executive Risk View](02-risk-and-controls/executive-risk-view.md) - current risk and remediation position
2. [Risk Register](02-risk-and-controls/risk-register.csv) - risk statements, scoring, treatment, and ownership
3. [Access Review Workpaper](03-assessment-and-evidence/access-review-workpaper.md) - completed control testing and exceptions
4. [Remediation Validation](04-remediation-and-validation/remediation-validation.md) - retest and evidence-backed closure

## Explore the project

### [01 - Context and Governance](01-context-and-governance/)

Understand the scenario, system relationships, policy, and who is accountable for the work.

- [Project Overview](01-context-and-governance/project-overview.md)
- [System Context](01-context-and-governance/system-context.md)
- [Security Policy](01-context-and-governance/security-policy.md)
- [Responsibility Matrix](01-context-and-governance/responsibility-matrix.md)

### [02 - Risk and Controls](02-risk-and-controls/)

See how the five risks are prioritized, scored, assigned, and connected to NIST controls.

- [Risk Summary](02-risk-and-controls/risk-summary.md)
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

```text
System context
→ risk
→ risk owner and risk action owner
→ control
→ evidence
→ assessment workpaper
→ finding
→ remediation
→ retest
→ executive reporting
```

A closed finding does not automatically close the larger risk. The risk stays open until there is enough evidence to support that decision.
