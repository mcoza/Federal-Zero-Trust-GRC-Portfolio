# Federal Zero Trust GRC Portfolio

A graduate capstone-derived governance, risk, and compliance portfolio modeling unauthorized-access risk in a fictional civilian federal environment.

The project translates academic cybersecurity work into practical GRC deliverables: risk identification, control mapping, remediation tracking, policy development, and evidence planning.

> **Portfolio demonstration only.** This repository contains no sensitive, proprietary, or real federal agency data. It represents academic/portfolio work, not professional federal GRC experience.

## Scenario

The modeled environment includes internal users, privileged administrators, remote access users, application servers, file shares, logging systems, backup systems, network infrastructure, and segmented network zones.

The security objective is to reduce unauthorized access and data exposure through Zero Trust-aligned controls across identity, access governance, privileged access, network segmentation, remote access, logging, and backup validation.

## Frameworks referenced

- NIST SP 800-53 Rev. 5
- NIST SP 800-37 Rev. 2 Risk Management Framework concepts
- NIST Cybersecurity Framework
- NIST SP 800-207 Zero Trust Architecture
- CISA Zero Trust Maturity Model

## Portfolio snapshot

- **Risks identified:** 5
- **High risks:** 4
- **POA&M items:** 5
- **Evidence items:** 8
- **Primary control framework:** NIST SP 800-53 Rev. 5

## Artifacts

| # | Artifact | What it demonstrates | RMF tie-in |
|---|---|---|---|
| 00 | [Portfolio Overview](artifacts/00-portfolio-overview.md) | Project scope, framework references, security themes, and artifact relationships | Overall context |
| 01 | [Executive Risk Summary](artifacts/01-executive-risk-summary.md) | Leadership-facing business impact, key risks, recommendations, and expected outcome | Authorize |
| 02 | [Risk Register](artifacts/02-risk-register.csv) | Risk statements, assets, threats, vulnerabilities, scoring, treatment, ownership, and evidence needs | Categorize / Assess |
| 02A | [Risk Scoring Guide](artifacts/02-risk-scoring-guide.md) | 5×5 likelihood/impact methodology and rating thresholds | Assess |
| 03 | [Control Mapping Matrix](artifacts/03-control-mapping-matrix.csv) | Risk-to-control mapping, implementation expectations, evidence needs, owners, and status | Select |
| 03A | [Control Mapping Method](artifacts/03-control-mapping-method.md) | Method used to select controls and define implementation/evidence expectations | Select |
| 04 | [POA&M-Style Remediation Tracker](artifacts/04-poam-remediation-tracker.csv) | Findings, milestones, owners, target dates, status, and closure evidence | Monitor |
| 04A | [POA&M Method](artifacts/04-poam-method.md) | Remediation-tracking flow and status definitions | Monitor |
| 05 | [Access Control & Network Segmentation Policy](artifacts/05-access-control-segmentation-policy.md) | Policy requirements for access, segmentation, remote access, monitoring, backups, and exceptions | Implement |
| 06 | [Evidence Checklist](artifacts/06-evidence-checklist.csv) | Audit/control evidence requirements, validation methods, owners, and review frequency | Assess |

## Risk themes

1. Excessive user access beyond role requirements
2. Weak privileged access separation and monitoring
3. Insufficient internal network segmentation
4. Incomplete SIEM/logging coverage
5. Unvalidated backup and restore processes

## GRC workflow represented

```text
Identify risk
    ↓
Score and prioritize
    ↓
Map to NIST controls
    ↓
Define implementation expectations
    ↓
Track remediation through POA&M-style items
    ↓
Identify validation evidence
    ↓
Review residual/remaining risk
```

## Repository purpose

The repository is intentionally self-contained so the portfolio can be reviewed directly in GitHub without requiring access to the original Google Drive workspace. The source documents and spreadsheets remain the working originals; the files here are portfolio-readable representations of those artifacts.
