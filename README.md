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

1. [Executive Risk View](artifacts/01A-executive-risk-view.md) - current risk and remediation position
2. [Risk Register](artifacts/02-risk-register.csv) - risk statements, scoring, treatment, and ownership
3. [Access Review Workpaper](artifacts/07B-access-review-workpaper.md) - completed control testing and exceptions
4. [Remediation Validation](artifacts/08-remediation-validation.md) - retest and evidence-backed closure

## Files

| # | File | What it is for |
|---|---|---|
| 00 | [Project Overview](artifacts/00-project-overview.md) | Scenario, scope, frameworks, governance roles, and Zero Trust relationships |
| 00A | [System Context](artifacts/00A-system-context.md) | Logical environment view showing where the five risks sit |
| 01 | [Risk Summary](artifacts/01-risk-summary.md) | Why the risks are ranked as they are and what the evidence currently supports |
| 01A | [Executive Risk View](artifacts/01A-executive-risk-view.md) | Heatmap, current risk position, remediation status, and management attention |
| 02 | [Risk Register](artifacts/02-risk-register.csv) | Risk statements, scores, rationale, treatment, ownership, status, and evidence needs |
| 02A | [Risk Scoring](artifacts/02-risk-scoring.md) | How I score and rank the risks |
| 03 | [Control Mapping](artifacts/03-control-mapping.csv) | Which controls matter, what I am checking, and what evidence I would review |
| 03A | [Control Mapping Notes](artifacts/03-control-mapping-notes.md) | How I choose controls and keep the mapping tied to evidence |
| 04 | [Remediation Tracker](artifacts/04-remediation-tracker.csv) | Issues, related controls, owners, milestones, dates, status, closure requirements, and evidence |
| 04A | [Remediation Process](artifacts/04-remediation-process.md) | How I move an issue from open to validated closure |
| 05 | [Security Policy](artifacts/05-security-policy.md) | Security requirements and responsibilities for the scenario |
| 05A | [Responsibility Matrix](artifacts/05A-responsibility-matrix.md) | RACI for risk, governance, assessment, and technical activities |
| 06 | [Evidence Review](artifacts/06-evidence-review.csv) | What evidence I would ask for and how I would check it |
| 07 | [Access Review](artifacts/07-access-review.csv) | Fictional user access records used in the completed review |
| 07A | [Access Control Review](artifacts/07-access-control-review.md) | Assessment narrative, exceptions, conclusion, and remediation trace |
| 07B | [Access Review Workpaper](artifacts/07B-access-review-workpaper.md) | Population, testing procedure, account-level results, and workpaper conclusion |
| 08 | [Access Retest](artifacts/08-access-retest.csv) | Updated access after the two exceptions were corrected |
| 08A | [Remediation Validation](artifacts/08-remediation-validation.md) | The retest and closure decision for POAM-001 |

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
