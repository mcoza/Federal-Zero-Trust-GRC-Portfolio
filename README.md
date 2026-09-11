# Federal Zero Trust GRC Portfolio

**IT Risk Assessment, Control Testing, Evidence Review, and Remediation**

This repo started as my graduate cybersecurity capstone. I rebuilt it around a fictional civilian federal environment so I could work through the GRC side of real security problems.

I use the scenario to write and prioritize risks, assign ownership, choose controls that fit, decide what evidence matters, document findings, and follow remediation through validation.

NIST SP 800-53 Rev. 5 is the main control framework. NIST SP 800-37, NIST SP 800-53A, the NIST Cybersecurity Framework 2.0, NIST SP 800-207, and the CISA Zero Trust Maturity Model provide supporting risk, assessment, governance, and Zero Trust context.

## What is in the repo

The project covers five risk areas:

- excessive user access
- privileged access governance
- network segmentation and remote access
- SIEM and logging coverage
- backup and restore validation

Across those areas, the repo includes risk scoring, control mapping, evidence planning, a security policy, a responsibility matrix, remediation tracking, executive reporting, and one access-control review carried through retesting and closure.

## Current snapshot

- **Risks:** 5
- **High initial risks:** 4
- **POA&M items:** 5 (1 closed, 4 open)
- **Evidence requirements:** 8
- **Completed control assessments:** 1
- **Completed remediation retests:** 1

## Files

| # | File | What it is for |
|---|---|---|
| 00 | [Project Overview](artifacts/00-project-overview.md) | Scenario, scope, frameworks, governance roles, and Zero Trust relationships |
| 01 | [Risk Summary](artifacts/01-risk-summary.md) | Priority risks, business impact, ownership, completed review, and next actions |
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
| 07A | [Access Control Review](artifacts/07-access-control-review.md) | How I tested the access records and documented the exceptions |
| 08 | [Access Retest](artifacts/08-access-retest.csv) | Updated access after the two exceptions were corrected |
| 08A | [Remediation Validation](artifacts/08-remediation-validation.md) | The retest and closure decision for POAM-001 |

## How the pieces fit together

```text
Risk
→ risk owner and risk action owner
→ control
→ what should be true
→ evidence
→ review
→ finding
→ remediation
→ retest
→ reporting
```

A closed finding does not automatically close the larger risk. The risk stays open until there is enough evidence to support that decision.
