# Controls Catalog (v1)
## Alyssa Solen | AI Governance Operating System

This catalog defines the minimum controls required by risk tier. Controls are written to be auditable and operational.

## How to use this catalog
1. Assign a tier using `docs/02_risk_tiering.md`
2. Implement all controls required for that tier
3. Produce the evidence artifacts listed for each control
4. Store evidence in the use case record (issue + linked files) and keep registers updated

## Control families
A. Ownership and accountability  
B. Inventory and documentation  
C. Data governance and privacy  
D. Security and access control  
E. Evaluation and quality thresholds  
F. Safety, abuse, and misuse resistance  
G. Monitoring, drift, and observability  
H. Change control and release management  
I. Incident response and postmortems  
J. Vendor and third-party governance  
K. Audit evidence and retention

---

# Tier 1 Controls (Low impact decision support)
## A1. Named owners
- Requirement: business owner and technical owner assigned
- Evidence: intake record includes owners

## B1. Use case inventory entry
- Requirement: registered in `registers/ai_inventory.csv`
- Evidence: inventory row with tier, owners, status, last review date

## B2. Basic documentation
- Requirement: documented purpose, deployment surface, model used, data sources
- Evidence: completed `templates/use_case_intake.md`

## C1. Data handling constraints
- Requirement: define what data is allowed and prohibited (including PII handling)
- Evidence: data section in intake, plus `templates/data_sheet.md` if needed

## E1. Human review requirement for external impact
- Requirement: outputs that affect external parties must be reviewed by a human
- Evidence: documented review rule in intake and workflow

## G1. Basic logging and retention (where feasible)
- Requirement: log prompts/outputs or interaction metadata to support troubleshooting
- Evidence: monitoring plan includes what is logged and retention period

## H1. Change recording
- Requirement: record significant prompt/model changes
- Evidence: change request issue or changelog entry

Minimum Tier 1 evidence set:
- use case intake
- inventory row
- monitoring plan (basic)
- change log entry when applicable

---

# Tier 2 Controls (Medium impact operational influence)
Tier 2 includes all Tier 1 controls plus the following.

## A2. Governance review required
- Requirement: governance review group signoff before release
- Evidence: approval recorded in the use case record

## B3. Model card (lightweight)
- Requirement: document model identity, intended use, limitations, and failure modes
- Evidence: `templates/model_card.md`

## C2. Data sheet (required)
- Requirement: document data sources, permissions, retention, and prohibited data
- Evidence: `templates/data_sheet.md`

## D1. Access control
- Requirement: define who can change prompts, models, and routing logic
- Evidence: documented access list and process

## E2. Evaluation plan and thresholds (required)
- Requirement: predefine metrics and acceptance thresholds
- Evidence: `templates/evaluation_plan.md`

## E3. Regression testing on changes
- Requirement: rerun evaluation plan for any behavioral change
- Evidence: evaluation results attached to change request

## F1. Abuse and misuse checks
- Requirement: test for basic misuse relevant to the domain (prompt injection, sensitive content, policy bypass)
- Evidence: test cases referenced in evaluation results

## G2. Monitoring plan (required)
- Requirement: monitor quality, safety, and drift signals with alert thresholds
- Evidence: `templates/monitoring_plan.md`

## H2. Rollback plan (required)
- Requirement: documented rollback triggers and rollback owner
- Evidence: rollback section in monitoring plan and release checklist

Minimum Tier 2 evidence set:
- Tier 1 evidence
- model card
- data sheet
- evaluation plan and results
- monitoring plan with thresholds
- governance signoff recorded

---

# Tier 3 Controls (High impact, regulated, rights-affecting, safety-critical)
Tier 3 includes all Tier 2 controls plus the following. Tier 3 is “prove control at all times.”

## A3. Formal accountability and escalation
- Requirement: executive sponsor identified and escalation path documented
- Evidence: charter mapping or use case record includes sponsor and escalation path

## B4. Full documentation set
- Requirement: full model card and full data sheet, plus decision logic documentation
- Evidence: model card, data sheet, plus any system diagrams or decision flow notes

## D2. Security review
- Requirement: security review required for deployment and for material changes
- Evidence: security signoff recorded, security findings tracked if applicable

## E4. Strong evaluation requirements
- Requirement: expanded test coverage including edge cases and failure mode testing
- Evidence: evaluation results include edge case coverage and documented blockers

## F2. Adversarial testing required
- Requirement: adversarial testing appropriate to the domain and deployment surface
- Evidence: documented adversarial test plan and results

## F3. Human-in-the-loop constraints (default)
- Requirement: human-in-the-loop for final decisions unless explicitly justified and approved
- Evidence: documented decision boundary and approval if automation is proposed

## G3. Continuous monitoring with rapid response
- Requirement: continuous or high-frequency monitoring, alerting, and on-call ownership
- Evidence: monitoring plan includes frequency, alert routing, and response SLA

## H3. Strict change control
- Requirement: no rollout of behavior changes without approval and validated evaluation
- Evidence: change request issue with signoff and evaluation artifacts attached

## I1. Incident response playbook enforced
- Requirement: incident classification, containment steps, communications path, postmortem required
- Evidence: incident template used, postmortem completed, corrective actions tracked

## J1. Vendor governance (if third-party)
- Requirement: vendor disclosures, update notifications, data handling terms, and audit rights where possible
- Evidence: vendor review record and contract notes captured in the use case record

Minimum Tier 3 evidence set:
- Tier 2 evidence
- executive sponsor and escalation path
- adversarial test results
- strict change control records
- continuous monitoring and response SLA
- incident playbook usage when applicable
- vendor governance record if relevant

---

# Evidence mapping (what to produce)
For each use case, maintain these artifacts as applicable:
- Use case intake: `templates/use_case_intake.md`
- Risk assessment: `templates/risk_assessment.md`
- Model card: `templates/model_card.md`
- Data sheet: `templates/data_sheet.md`
- Evaluation plan: `templates/evaluation_plan.md`
- Release checklist: `templates/release_checklist.md`
- Monitoring plan: `templates/monitoring_plan.md`
- Exception request: `templates/exception_request.md`
- Incident postmortem: `templates/incident_postmortem.md`

Registers to keep current:
- `registers/ai_inventory.csv`
- `registers/risk_register.csv`
- `registers/exceptions.csv`

## Attribution
This work is authored by **Alyssa Solen**. Any reuse, adaptation, or derivative governance program based on this repository must include clear attribution to Alyssa Solen in documentation and materials where the framework appears.
