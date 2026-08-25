# Federal Zero Trust GRC Portfolio

A GRC portfolio based on my graduate cybersecurity capstone and built around a fictional civilian federal environment.

The project shows how I went from identifying security issues to documenting risk, choosing controls, reviewing evidence, finding exceptions, and tracking remediation.

> **Portfolio demonstration only.** This repository contains no sensitive, proprietary, or real federal agency data. It represents academic and portfolio work, not professional federal GRC experience.

## What this portfolio shows

- risk identification and prioritization
- NIST SP 800-53 Rev. 5 control mapping
- risk scoring with written rationale
- evidence planning
- one control assessment using synthetic access data
- remediation tracking through a POA&M-style artifact
- policy requirements and a limited Zero Trust crosswalk

NIST SP 800-53 is the main control framework. NIST SP 800-37, NIST SP 800-53A, NIST SP 800-207, and the CISA Zero Trust Maturity Model are supporting references where they fit the work shown here.

This is not a complete federal RMF package or a full Zero Trust maturity assessment.

## Reasoning flow

```mermaid
flowchart TD
    A[Understand the environment] --> B[Identify a security condition or weakness]
    B --> C[Identify the affected asset or business area]
    C --> D[Determine what could happen]
    D --> E[Write the risk statement]
    E --> F[Score likelihood and impact with rationale]
    F --> G[Prioritize the risk]
    G --> H[Select a relevant control]
    H --> I[Define the expected control condition]
    I --> J[Identify evidence]
    J --> K[Examine or test the evidence]
    K --> L{Does the evidence meet the condition?}
    L -->|Yes| M[Document the conclusion]
    L -->|No| N[Document the finding]
    N --> O[Define remediation]
    O --> P[Assign an action owner and target date]
    P --> Q[Collect closure evidence]
    Q --> R[Retest or validate]
    R --> S{Corrected?}
    S -->|Yes| M
    S -->|No| O
    M --> T[Update the risk picture and report the result]
```

The main point is simple: evidence is not proof by itself. I have to compare it with an expected condition before I can support a control conclusion or finding.

## Current portfolio snapshot

- **Risks identified:** 5
- **High risks:** 4
- **POA&M items:** 5
- **Evidence items:** 8
- **Control assessments:** 1
- **Access review exceptions:** 2

## Artifacts

| # | Artifact | What it shows |
|---|---|---|
| 00 | [Portfolio Overview](artifacts/00-portfolio-overview.md) | Scenario, scope, framework use, and methodology |
| 01 | [Executive Risk Summary](artifacts/01-executive-risk-summary.md) | Priority risks, business impact, and recommended actions |
| 02 | [Risk Register](artifacts/02-risk-register.csv) | Risk statements, scores, rationale, treatment, owners, and evidence needs |
| 02A | [Risk Scoring Guide](artifacts/02-risk-scoring-guide.md) | 5x5 scoring method and rating thresholds |
| 03 | [Control Mapping Matrix](artifacts/03-control-mapping-matrix.csv) | Risk-to-control mapping, expected implementation, evidence, and status |
| 03A | [Control Mapping Method](artifacts/03-control-mapping-method.md) | How I selected controls and traced them to evidence and remediation |
| 04 | [POA&M-Style Remediation Tracker](artifacts/04-poam-remediation-tracker.csv) | Findings, milestones, owners, dates, and closure evidence |
| 04A | [POA&M Method](artifacts/04-poam-method.md) | Remediation and closure logic |
| 05 | [Security Control Policy](artifacts/05-security-control-policy.md) | Control requirements and responsibilities for the scenario |
| 06 | [Evidence Checklist](artifacts/06-evidence-checklist.csv) | Expected control conditions, evidence artifacts, and validation methods |
| 07 | [Access Review Evidence](artifacts/07-synthetic-access-review.csv) | Synthetic account and group data used in the assessment |
| 07A | [Control Assessment](artifacts/07-control-assessment.md) | AC-6 assessment criteria, exceptions, conclusion, and remediation traceability |

## Example: R-001 from risk to remediation

```text
R-001 Excessive user access
        ↓
AC-6 Least Privilege
        ↓
Expected condition: access matches approved role
        ↓
Synthetic access evidence
        ↓
2 of 12 records contain unsupported access
        ↓
Assessment finding: Other Than Satisfied
        ↓
POAM-001
        ↓
Correct access, retain evidence, and retest before closure
```

## What this project does not cover

The portfolio does not include a complete system categorization, control baseline tailoring package, SSP, SAP, SAR, authorization decision, or continuous monitoring program.

I also do not assign residual risk just because remediation is planned. I would revisit residual risk after there is evidence that the controls are implemented and working.