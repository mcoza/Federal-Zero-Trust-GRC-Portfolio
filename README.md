# Federal Zero Trust GRC Portfolio

**IT Risk Assessment, Control Testing, Evidence Review, and Remediation**

This repo started as my graduate cybersecurity capstone. I rebuilt it as a hands-on GRC portfolio around a fictional civilian federal environment.

The goal is simple: show how I work through security problems from the GRC side. That means writing and prioritizing risks, choosing controls that actually fit, deciding what evidence would matter, documenting findings, and following remediation through validation.

I use NIST SP 800-53 Rev. 5 as the main control framework. NIST SP 800-37, NIST SP 800-53A, NIST SP 800-207, and the CISA Zero Trust Maturity Model provide supporting risk, assessment, and Zero Trust context.

## What is in the repo

The project covers five risk areas:

- excessive user access
- privileged access governance
- network segmentation and remote access
- SIEM and logging coverage
- backup and restore validation

Across those areas, the repo includes risk scoring, control mapping, evidence planning, a security policy, remediation tracking, executive reporting, and one worked access-control review carried through retesting and closure.

## Current snapshot

- **Risks:** 5
- **High initial risks:** 4
- **POA&M items:** 5 (1 closed, 4 open)
- **Evidence requirements:** 8
- **Completed control assessments:** 1
- **Completed remediation retests:** 1

## Artifacts

| # | Artifact | What it is for |
|---|---|---|
| 00 | [Project Overview](artifacts/00-project-overview.md) | Scenario, scope, framework use, and Zero Trust relationships |
| 01 | [Risk Summary](artifacts/01-risk-summary.md) | Priority risks, business impact, completed assessment result, and next actions |
| 02 | [Risk Register](artifacts/02-risk-register.csv) | Risk statements, scores, rationale, treatment, owners, and evidence needs |
| 02A | [Risk Scoring](artifacts/02-risk-scoring.md) | The 5x5 scoring method I use to rank the risks |
| 03 | [Control Mapping](artifacts/03-control-mapping.csv) | Risk-to-control mapping, expected conditions, evidence, and status |
| 03A | [Control Mapping Notes](artifacts/03-control-mapping-notes.md) | How I decide which controls belong and what would count as evidence |
| 04 | [Remediation Tracker](artifacts/04-remediation-tracker.csv) | Findings, owners, milestones, dates, status, and closure evidence |
| 04A | [Remediation Process](artifacts/04-remediation-process.md) | How I move a weakness from open to validated closure |
| 05 | [Security Policy](artifacts/05-security-policy.md) | Security requirements and responsibilities for the scenario |
| 06 | [Evidence Review](artifacts/06-evidence-review.csv) | What evidence I would ask for and how I would review it |
| 07 | [Access Review](artifacts/07-access-review.csv) | Fictional account and group data used in the completed review |
| 07A | [Access Control Review](artifacts/07-access-control-review.md) | The worked assessment, findings, and remediation link |
| 08 | [Access Retest](artifacts/08-access-retest.csv) | Updated access data after the two exceptions were corrected |
| 08A | [Remediation Validation](artifacts/08-remediation-validation.md) | The retest and closure decision for POAM-001 |

## How the pieces fit together

```text
Risk
→ control
→ expected condition
→ evidence
→ assessment
→ finding
→ remediation
→ validation
→ reporting
```

I kept the project small enough that those connections are easy to follow. A closed finding does not automatically mean the larger risk is gone; the risk stays open until there is enough evidence to support that conclusion.
