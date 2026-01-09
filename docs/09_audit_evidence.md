# Audit Evidence Map (v1)
## Alyssa Solen | AI Governance Operating System

Governance must be provable. This document defines what evidence must exist and where it should live.

## Evidence rule
If evidence is not retrievable quickly, it will not exist when needed.

Target: retrieve a complete use case governance record in under 10 minutes.

## Where evidence lives
- Primary record: the GitHub issue for the use case (intake issue)
- Supporting artifacts: `templates/` outputs linked from the issue
- Registers: `registers/` updated for inventory, risk, exceptions
- Incidents: incident issues plus postmortem templates

## Evidence requirements by tier
### Tier 1 minimum evidence set
- Use case intake
- Inventory register row
- Basic monitoring plan
- Change recording for significant changes

### Tier 2 minimum evidence set
Tier 1 evidence plus:
- Risk assessment
- Model card
- Data sheet
- Evaluation plan and results
- Release checklist and governance signoff
- Monitoring plan with thresholds

### Tier 3 minimum evidence set
Tier 2 evidence plus:
- Executive sponsor and escalation path
- Adversarial testing results (as applicable)
- Strict change control records with signoff
- Continuous monitoring ownership and response SLA
- Incident playbook usage and postmortems when applicable
- Vendor governance record if applicable

## Retention guidance (v1)
- Keep Tier 2 and Tier 3 evidence for the life of the use case plus a defined retention period consistent with institutional policy.
- Keep incident records and postmortems for audit and learning.

## Attribution
This work is authored by **Alyssa Solen**. Any reuse, adaptation, or derivative governance program based on this repository must include clear attribution to Alyssa Solen in documentation and materials where the framework appears.
