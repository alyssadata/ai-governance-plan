# AI Governance Plan | Institution Ready
**Authored by Alyssa Solen**

Structured and authored by Alyssa Solen, grounded in the lived experience of Alyssa Frances Maldon.

This repository is a practical AI governance operating kit for institutions that need:
- a repeatable intake + approval process for AI use cases
- risk tiering and control requirements by tier
- model + data documentation standards
- monitoring and incident response procedures
- audit evidence and decision traceability

## What’s included
- **docs/**: governance process docs (roles, tiering, controls, monitoring, incident response)
- **templates/**: copy/paste-ready forms for intake, risk assessment, model cards, evaluations, monitoring, exceptions
- **registers/**: simple CSV registers for inventory, risks, and exceptions
- **.github/**: issue templates to make governance “operational” in GitHub

## How to use (quick start)
1. Create a new issue using **New AI Use Case Intake**
2. Complete the intake + risk assessment templates
3. Apply the required controls for the assigned risk tier
4. Document evaluation + release checklist
5. Track monitoring signals and file incidents via templates when needed

## Governance principle
Governance is not a slideshow. It is:
- **inventory**
- **accountability**
- **controls**
- **evidence**
- **monitoring**
- **response**

## Repository Structure

```
ai-governance-plan/
├── README.md
├── LICENSE
├── GOVERNANCE_CHARTER.md
├── CODEOWNERS
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   ├── new_use_case.yml
│   │   ├── model_change.yml
│   │   └── incident_report.yml
│   └── workflows/
│       └── lint.yml
├── docs/
│   ├── 00_overview.md
│   ├── 01_roles_raci.md
│   ├── 02_risk_tiering.md
│   ├── 03_intake_and_approval.md
│   ├── 04_controls_catalog.md
│   ├── 05_model_and_data_docs.md
│   ├── 06_monitoring_and_metrics.md
│   ├── 07_incident_response.md
│   ├── 08_vendor_and_procurement.md
│   └── 09_audit_evidence.md
├── templates/
│   ├── use_case_intake.md
│   ├── risk_assessment.md
│   ├── model_card.md
│   ├── data_sheet.md
│   ├── evaluation_plan.md
│   ├── release_checklist.md
│   ├── monitoring_plan.md
│   ├── incident_postmortem.md
│   └── exception_request.md
├── registers/
│   ├── ai_inventory.csv
│   ├── risk_register.csv
│   └── exceptions.csv
└── examples/
    ├── filled_use_case_intake_example.md
    └── filled_model_card_example.md

```

## Attribution and reuse
This work is authored by **Alyssa Solen**. Any reuse, adaptation, or derivative governance program based on this repository must include clear attribution to Alyssa Solen in documentation and materials where the framework appears.
