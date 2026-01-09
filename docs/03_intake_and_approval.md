# Intake and Approval Workflow (v1)
## Alyssa Solen | AI Governance Operating System

This document defines the operational workflow that turns governance from policy into execution.

## Overview
Every AI use case moves through:
1) Intake  
2) Risk tier assignment  
3) Control implementation  
4) Evaluation and acceptance  
5) Approval and release  
6) Monitoring and periodic review  
7) Change control (whenever anything changes)  
8) Incident response (when something goes wrong)

Governance is complete only when evidence exists for each step.

## Intake (required for all use cases)
### Intake entry must include
- use case name and summary
- business owner (accountable)
- technical owner (accountable)
- deployment surface (internal, customer-facing, API, embedded)
- model details (vendor or name, version if known)
- data sources used
- whether it uses PII or sensitive data
- whether it influences eligibility, rights, safety, finance, healthcare, employment, or regulated outcomes
- proposed tier with rationale
- planned controls and evidence artifacts
- monitoring owner and rollback plan

### Output artifact
- `templates/use_case_intake.md` completed and stored as the governance record (issue body or linked file)

## Risk tier assignment
### Tier assignment process
- Assign tier using `docs/02_risk_tiering.md`
- Default to the higher tier if uncertain
- If the use case is customer-facing, regulated, or rights-affecting, it is never Tier 0

### Tier decision record must include
- assigned tier
- rationale
- key risk indicators triggering the tier
- required controls list for the tier
- who approved the tier assignment

### Output artifact
- completed `templates/risk_assessment.md` (or equivalent tier decision record)

## Control implementation
Controls are mandatory requirements matched to tier. Controls are not optional.

### Output artifacts (by tier)
- Tier 1: minimum evidence set for data handling, review, and basic logging
- Tier 2: evaluation plan, monitoring plan, rollback plan, plus Tier 1 evidence
- Tier 3: formal signoff, adversarial testing, robust documentation, continuous monitoring, strict change control

Control requirements are defined in `docs/04_controls_catalog.md`.

## Evaluation and acceptance
### Evaluation must be defined before release
Evaluation is not a retrospective justification. It is a pre-declared standard.

Evaluation must include:
- success metrics and minimum acceptance thresholds
- test set description (and provenance if relevant)
- safety and abuse tests appropriate to the tier
- bias or fairness checks where relevant
- latency and reliability requirements where relevant
- failure modes and what is considered a blocker

### Output artifacts
- `templates/evaluation_plan.md`
- evaluation results (linked file or stored in a governance issue comment)
- Tier 3 requires explicit “pass” signoff recorded

## Approval and release
### Approval gates by tier
- Tier 0: normal engineering release process
- Tier 1: business owner + technical owner signoff
- Tier 2: business owner + technical owner + governance review signoff
- Tier 3: business owner + technical owner + governance review signoff + legal/compliance and security signoff as applicable

### Release requirements
Before release, the record must show:
- completed intake
- tier assignment with rationale
- controls implemented with evidence
- evaluation completed and passed
- monitoring plan and rollback plan confirmed
- named owners for monitoring and incident response

### Output artifact
- `templates/release_checklist.md` completed and linked to the use case record

## Monitoring and periodic review
### Monitoring is mandatory
Monitoring must exist at launch, not after the first incident.

Monitoring must include:
- what signals are tracked (quality, safety, abuse, drift, performance)
- alert thresholds and escalation path
- monitoring owner and response SLA
- rollback triggers and rollback owner
- log retention and access policy

### Review cadence
- Tier 1: review at least quarterly
- Tier 2: review at least monthly
- Tier 3: review at least weekly, plus after any change or incident

### Output artifacts
- `templates/monitoring_plan.md`
- register updates (`registers/ai_inventory.csv` and `registers/risk_register.csv`)
- review notes recorded as an issue comment or linked artifact

## Change control (this is where governance usually fails)
Any of the following triggers change control:
- model swap or version change
- prompt change that affects behavior (system prompt, tools, policies, routing logic)
- data source change or permission change
- retraining, fine-tuning, RAG index updates, embedding changes
- new deployment surface (internal to external, or new customer segment)
- new automation level (suggestion to automated action)
- vendor product update that changes model behavior

### Change control rule
No behavioral change without a recorded change request and tier-appropriate evaluation.

### Change control by tier
- Tier 1: record change, spot-check evaluation, update documentation
- Tier 2: record change, rerun evaluation plan, update monitoring thresholds if needed
- Tier 3: formal review, adversarial testing as needed, explicit signoff before rollout

### Output artifact
- `.github/ISSUE_TEMPLATE/model_change.yml` or equivalent change request issue
- updated evidence artifacts and register updates

## Exceptions
Exceptions are allowed only with:
- explicit business justification
- compensating controls
- an expiry date
- named owner responsible for closure
- governance approval

### Output artifact
- `templates/exception_request.md`
- entry in `registers/exceptions.csv`

## Recordkeeping and audit readiness
For each use case, the governance record must be retrievable in under 10 minutes.

Required evidence set is defined in `docs/09_audit_evidence.md`.

## Attribution
This work is authored by **Alyssa Solen**. Any reuse, adaptation, or derivative governance program based on this repository must include clear attribution to Alyssa Solen in documentation and materials where the framework appears.
