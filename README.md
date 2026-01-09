# Alyssa Solen | AI Governance Operating System

**Authored by Alyssa Solen**  
Structured and authored by Alyssa Solen, grounded in the lived experience of Alyssa Frances Maldon.

## What this is
This repository is a practical AI governance operating system for institutions that need to prove control over AI systems across the full lifecycle.

Governance here is not a slide deck. It is:
- inventory
- accountability
- controls
- evidence
- monitoring
- incident response

If you cannot show it in an audit trail, you do not have governance.

## Who this is for
- institutions deploying AI in products, operations, or decision support
- risk, compliance, security, and engineering teams who need a shared operating model
- leaders who need a repeatable way to approve, monitor, and explain AI use

## What’s included
- **docs/**: the operating model (roles, tiering, controls, approvals, monitoring, incidents, audit evidence)
- **templates/**: copy/paste-ready forms for intake, risk assessment, model cards, evaluation plans, monitoring plans, exceptions, postmortems
- **registers/**: lightweight CSV registers for inventory, risk, and exceptions
- **.github/**: issue templates to run governance in GitHub (intake, change control, incident reporting)

## Quick start
1. Create a new issue using the **New AI Use Case Intake** template.
2. Complete the intake and assign a risk tier.
3. Implement the required controls for that tier.
4. Produce the required evidence artifacts (templates).
5. Launch with monitoring and a rollback plan.
6. File incidents and postmortems using the repo templates.

## Core governance loop
1) **Intake**: define the use case, owners, model, data, and impact  
2) **Tier**: assign risk tier using consistent criteria  
3) **Controls**: apply control requirements by tier  
4) **Evidence**: generate artifacts that prove due diligence  
5) **Monitor**: detect drift, failures, and misuse  
6) **Respond**: escalate, contain, and document incidents  
7) **Review**: periodic reassessment and change control


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

## License
See `LICENSE`. If a conflict exists between convenience and authorship integrity, authorship integrity wins.
