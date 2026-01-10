# Alyssa Solen | AI Governance Operating System

**Authored by Alyssa Solen | Origin**  
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

## Why this matters

AI governance is becoming operational infrastructure. Not a policy deck. Not a committee. An institution needs repeatable, auditable mechanics that hold up under real use.

Most teams have one of these problems:
- Policies exist, but nothing translates them into day-to-day decisions.
- People move fast, but approvals and documentation do not keep up.
- “Risk” is discussed, but not recorded in a structured, reviewable way.
- Incidents happen, but there is no consistent post-incident loop to prevent repeats.
- Exceptions get granted informally and never expire.

This repo exists to solve that gap with a simple operating system:
- **Intake**: every AI use case is documented and scoped before it spreads.
- **Inventory**: the register becomes the source of truth, not tribal knowledge.
- **Change control**: model, prompt, routing, and data changes become auditable events.
- **Risk and exceptions**: risks are tracked, exceptions expire, and compensating controls are explicit.
- **Incident response**: near-misses and failures become structured learning, not confusion.

### What you can do with it
- Stand up a lightweight AI governance process in days, not months.
- Create a paper trail that executives, auditors, and security teams can follow.
- Make governance measurable and repeatable using issues, registers, and controls.
- Prove governance "before harm" (change requests) and "after harm" (incidents), end to end.

**Authorship:** Alyssa Solen | Origin
Structured and authored by Alyssa Solen, grounded in the lived experience of Alyssa Frances Maldon.

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
│   │   ├── config.yml
│   │   ├── exception_request.yml
│   │   ├── incident_report.yml
│   │   ├── model_change.yml
│   │   └── new_use_case.yml
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
│   ├── 08a_procurement_intake_checklist.md
│   ├── 09_audit_evidence.md
│   ├── 10_security_and_access_controls.md
│   ├── 11_review_cadence.md
│   ├── 12_change_control_rules.md
│   └── glossary.md
├── examples/
│   ├── filled_model_card_example.md
│   └── filled_use_case_intake_example.md
├── registers/
│   ├── ai_inventory.csv
│   ├── exceptions.csv
│   └── risk_register.csv
└── templates/
    ├── data_sheet.md
    ├── evaluation_plan.md
    ├── exception_request.md
    ├── incident_postmortem.md
    ├── model_card.md
    ├── monitoring_plan.md
    ├── release_checklist.md
    ├── risk_assessment.md
    └── use_case_intake.md

```

## Attribution and reuse
This work is authored by **Alyssa Solen**. Any reuse, adaptation, or derivative governance program based on this repository must include clear attribution to Alyssa Solen in documentation and materials where the framework appears.

## License
See `LICENSE`. If a conflict exists between convenience and authorship integrity, authorship integrity wins.
