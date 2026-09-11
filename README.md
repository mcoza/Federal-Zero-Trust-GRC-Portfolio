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

Across those areas, the repo includes risk scoring, control mapping, evidence planning, a security policy, remediation tracking, executive reporting, and one worked control assessment carried through retesting and closure.

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
| 00 | [Portfolio Overview](artifacts/00-portfolio-overview.md) | Scenario, scope, framework use, and Zero Trust relationships |
| 01 | [Executive Risk Summary](artifacts/01-executive-risk-summary.md) | Priority risks, business impact, completed assessment result, and next actions |
| 02 | [Risk Register](artifacts/02-risk-register.csv) | Risk statements, scores, rationale, treatment, owners, and evidence needs |
| 02A | [Risk Scoring Guide](artifacts/02-risk-scoring-guide.md) | The 5x5 scoring method I use to rank the risks |
| 03 | [Control Mapping Matrix](artifacts/03-control-mapping-matrix.csv) | Risk-to-control mapping, expected conditions, evidence, and status |
| 03A | [Control Mapping Method](artifacts/03-control-mapping-method.md) | How I decide which controls belong and what would count as evidence |
| 04 | [POA&M-Style Remediation Tracker](artifacts/04-poam-remediation-tracker.csv) | Findings, owners, milestones, dates, status, and closure evidence |
| 04A | [POA&M Method](artifacts/04-poam-method.md) | How I move a weakness from open to validated closure |
| 05 | [Security Control Policy](artifacts/05-security-control-policy.md) | Security requirements and responsibilities for the scenario |
| 06 | [Evidence Checklist](artifacts/06-evidence-checklist.csv) | What evidence I would ask for and how I would review it |
| 07 | [Access Review Evidence](artifacts/07-synthetic-access-review.csv) | Synthetic source data used in the completed control assessment |
| 07A | [Control Assessment](artifacts/07-control-assessment.md) | The worked assessment, findings, and remediation link |
| 08 | [Remediation Retest Evidence](artifacts/08-synthetic-access-retest.csv) | Updated evidence after the two access exceptions were corrected |
| 08A | [Retest and Validation](artifacts/08-retest-validation.md) | The retest and closure decision for POAM-001 |

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
