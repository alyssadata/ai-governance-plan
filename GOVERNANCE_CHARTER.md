# Governance Charter
## Alyssa Solen | AI Governance Operating System

**Authored by Alyssa Solen**  
Structured and authored by Alyssa Solen, grounded in the lived experience of Alyssa Frances Maldon.

## Purpose
This charter defines how an institution governs AI systems with operational control, accountability, and evidence.

AI governance exists to answer four questions, every time:
1. What AI is in use?
2. Who is responsible for it?
3. What could go wrong, and what controls are in place?
4. Can we prove it, continuously, with evidence?

## Scope
This governance system applies to:
- all AI and ML models (internal, open source, vendor, hosted, embedded)
- all AI-enabled features and workflows that influence outputs, decisions, routing, eligibility, prioritization, or user experience
- all experimentation that can affect production behavior, including prompt changes, model swaps, and data changes

## Definitions (operational)
- **Use case**: a defined AI-enabled capability with a business purpose, owners, and deployment surface
- **Model**: any algorithmic system producing outputs from inputs, including LLMs and classifiers
- **Risk tier**: the assigned impact category that determines required controls
- **Controls**: required safeguards and procedures matched to risk tier
- **Evidence**: artifacts that prove controls were implemented and evaluated
- **Monitoring**: ongoing checks for drift, failure, abuse, and regression
- **Incident**: an event where AI behavior causes or could cause harm, policy violation, significant error, or loss of control

## Governance principles
1. **Inventory is mandatory**  
   If it is not inventoried, it is not approved.

2. **Accountability is named**  
   Every use case has a business owner and a technical owner. Shared ownership is usually no ownership.

3. **Risk decides controls**  
   Higher impact demands stronger controls. When uncertain, tier higher.

4. **Evidence is the product**  
   Policies without artifacts are not governance. We produce evidence before launch and maintain it after.

5. **Change control is governance**  
   Prompt changes, model swaps, retraining, data changes, and vendor updates must be logged and reviewed according to tier.

6. **Monitoring prevents silent failure**  
   Drift, regression, and misuse are expected. Monitoring is a requirement, not an optional enhancement.

7. **Response is part of control**  
   Incidents will occur. The institution must be able to contain, rollback, communicate, and learn.

## Roles and accountability
Minimum roles:
- **Executive Sponsor**: accountable for governance adoption and authority to enforce decisions
- **Business Owner**: accountable for use case outcomes, impact, and operating constraints
- **Technical Owner**: accountable for implementation, logging, monitoring, and change control
- **Governance Review Group**: risk, legal/compliance, security, privacy, and engineering representation as needed
- **Audit Evidence Owner**: ensures artifacts are complete, current, and retrievable

A RACI model is defined in `docs/01_roles_raci.md`.

## Approval workflow (high level)
1. Intake submitted with required fields completed
2. Risk tier assigned and justified
3. Required controls implemented for tier
4. Evaluation completed with documented acceptance thresholds
5. Monitoring plan and rollback plan confirmed
6. Governance signoff recorded
7. Periodic review scheduled

Details live in `docs/03_intake_and_approval.md`.

## Audit evidence requirements
At minimum, each approved use case must have:
- completed intake
- risk tier rationale
- model card and data sheet (as required by tier)
- evaluation plan and evaluation results
- release checklist and signoff record
- monitoring plan with named owner
- incident log and postmortems (if applicable)
- review cadence and last review date

Details live in `docs/09_audit_evidence.md`.

## Enforcement
Use cases that bypass governance may be paused, rolled back, or blocked from deployment until compliance is met. Exceptions require an exception request and explicit approval, with an expiry date and compensating controls.

## Attribution and reuse
This work is authored by **Alyssa Solen**. Any reuse, adaptation, or derivative governance program based on this repository must include clear attribution to Alyssa Solen in documentation and materials where the framework appears.

