# Federal Zero Trust GRC Portfolio

**IT Risk Assessment, Control Testing, Evidence Review, and Remediation**

This portfolio demonstrates an IT risk and control assessment workflow in a fictional civilian federal environment.

The project focuses on identifying and prioritizing risk, mapping risks to security controls, defining evidence expectations, assessing selected control conditions, documenting findings, tracking remediation, validating corrective action, and reporting results.

NIST SP 800-53 Rev. 5 is the primary control framework. NIST SP 800-37, NIST SP 800-53A, NIST SP 800-207, and the CISA Zero Trust Maturity Model support the risk, assessment, and Zero Trust concepts used in the project.

## What this portfolio shows

- risk identification and prioritization
- 5x5 risk scoring with written rationale
- NIST SP 800-53 Rev. 5 control mapping
- evidence planning and validation criteria
- security policy requirements
- scoped control assessment and exception documentation
- POA&M-style remediation tracking
- remediation validation and closure
- executive risk reporting
- selected Zero Trust relationships across identity, networks, visibility, and governance

## Current portfolio snapshot

- **Risks identified:** 5
- **High initial risks:** 4
- **POA&M items:** 5 (1 closed, 4 open)
- **Evidence requirements defined:** 8
- **Completed control assessments:** 1
- **Completed remediation retests:** 1

## Artifacts

| # | Artifact | What it shows |
|---|---|---|
| 00 | [Portfolio Overview](artifacts/00-portfolio-overview.md) | Scenario, scope, framework use, and Zero Trust relationships |
| 01 | [Executive Risk Summary](artifacts/01-executive-risk-summary.md) | Priority risks, business impact, completed assessment result, and recommended actions |
| 02 | [Risk Register](artifacts/02-risk-register.csv) | Risk statements, scores, rationale, treatment, owners, and evidence needs |
| 02A | [Risk Scoring Guide](artifacts/02-risk-scoring-guide.md) | 5x5 scoring method and rating thresholds |
| 03 | [Control Mapping Matrix](artifacts/03-control-mapping-matrix.csv) | Risk-to-control mapping, expected implementation, evidence, and status |
| 03A | [Control Mapping Method](artifacts/03-control-mapping-method.md) | How controls are selected and traced to evidence and remediation |
| 04 | [POA&M-Style Remediation Tracker](artifacts/04-poam-remediation-tracker.csv) | Findings, source, milestones, owners, dates, status, and closure evidence |
| 04A | [POA&M Method](artifacts/04-poam-method.md) | Remediation and closure logic |
| 05 | [Security Control Policy](artifacts/05-security-control-policy.md) | Control requirements and responsibilities for the scenario |
| 06 | [Evidence Checklist](artifacts/06-evidence-checklist.csv) | Expected control conditions, evidence artifacts, and validation methods |
| 07 | [Access Review Evidence](artifacts/07-synthetic-access-review.csv) | Synthetic source data used in the completed control assessment |
| 07A | [Control Assessment](artifacts/07-control-assessment.md) | Assessment criteria, exceptions, conclusion, and remediation traceability |
| 08 | [Remediation Retest Evidence](artifacts/08-synthetic-access-retest.csv) | Updated evidence for the corrected exceptions |
| 08A | [Retest and Validation](artifacts/08-retest-validation.md) | Remediation validation and POAM-001 closure |

## How the artifacts connect

```text
Environment and risk
→ control selection
→ expected condition and evidence
→ assessment
→ finding or conclusion
→ remediation
→ validation
→ reporting
```

## Risk status

The risk register remains open where broader scenario conditions still require treatment or validation. Closing a specific finding does not by itself establish that the related broader risk has been reduced to an acceptable level.
