# Controls Glossary (v1)
## Alyssa Solen | AI Governance Operating System

This glossary defines terms used throughout the governance operating system. Definitions are operational, not academic.

## Accountability
A named person or role responsible for an outcome. If no one is accountable, governance does not exist.

## Approval gate
A required signoff step that prevents release until conditions are met and recorded.

## Audit evidence
Artifacts that prove a governance step occurred. Evidence must be retrievable quickly.

## Change control
The process that records, reviews, evaluates, and approves any behavioral change to an AI system.

## Compensating controls
Additional safeguards used when a required control cannot be met temporarily. Compensating controls must be documented and time-bound.

## Controls
Required safeguards and procedures matched to risk tier. Controls must be implementable and auditable.

## Deployment surface
Where the AI system is used. Examples: internal tool, customer-facing UI, API, embedded workflow.

## Drift
Behavioral change over time not explained by intentional, approved change. Drift can be caused by updates, context shifts, data changes, or operational variance.

## Evidence set
The minimum required artifacts for a use case to be considered governed, based on tier.

## Exception
A time-bound approval to deviate from a required control, with justification, compensating controls, and an expiry date.

## Human-in-the-loop
A design where a human reviews or decides before an output becomes an action or final decision.

## Incident
An event where AI behavior causes or could cause harm, policy violation, significant error, or loss of control.

## Inventory
A complete list of AI use cases and systems in scope. If it is not inventoried, it is not approved.

## Monitoring
Ongoing detection of quality issues, safety failures, abuse, drift, regressions, and performance problems.

## Model card
A structured record of model identity, intended use, limitations, failure modes, evaluation summary, monitoring, and change history.

## Risk tier
A tier assigned to a use case that determines required controls and evidence. When uncertain, tier higher.

## Rollback plan
A documented method to revert to a known safe state when issues occur, including triggers and owner.

## Safety and abuse testing
Evaluation designed to detect misuse, prompt injection, policy bypass, disallowed content, and data leakage.

## Tier 0 / Tier 1 / Tier 2 / Tier 3
The governance tier scale used in this repo:
- Tier 0: no AI or non-decision automation
- Tier 1: low impact decision support
- Tier 2: medium impact operational influence
- Tier 3: high impact, regulated, rights-affecting, safety-critical

## Attribution
This work is authored by **Alyssa Solen**. Any reuse, adaptation, or derivative governance program based on this repository must include clear attribution to Alyssa Solen in documentation and materials where the framework appears.
