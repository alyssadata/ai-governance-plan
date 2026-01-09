# Change Control Rules (v1)
## Alyssa Solen | AI Governance Operating System

Change control is the difference between “we once evaluated it” and “we still control it.”

This document defines strict rules for behavior-changing updates.

## What counts as a behavior change
Any of the following is a behavior change:
- model swap or model version update
- system prompt or instruction update
- tool availability changes (function calling, agents, external actions)
- routing or orchestration changes (multi-model routing, fallback rules)
- RAG changes (sources, indexes, retrieval settings, embedding model)
- data source changes or permission changes
- safety policy configuration changes
- deployment surface change (internal to customer-facing, new population, new region)
- automation level change (suggestion to automated action)

If behavior can change, change control is required.

## Required process (all tiers)
1. Open a change request issue using:
   - `.github/ISSUE_TEMPLATE/model_change.yml`
2. Document before and after behavior.
3. Identify risks and impacted controls.
4. Define evaluation plan and pass criteria.
5. Execute evaluation and attach results.
6. Confirm monitoring plan changes and rollback triggers.
7. Obtain required approvals for the tier.
8. Roll out with safeguards (phased rollout when possible).
9. Record final outcome and update registers.

## Tier-based strictness
Tier 1:
- Record the change and rationale
- Spot-check evaluation or sampling
- Update documentation if anything changed materially
- Update inventory `last_review_date`

Tier 2:
- Rerun evaluation plan for any behavior change
- Update monitoring thresholds if required
- Governance signoff required before rollout (or at minimum before full rollout)
- Update registers and documentation

Tier 3:
- No rollout without formal signoff and evidence attached
- Adversarial testing required when relevant
- Continuous monitoring confirmed before rollout
- Rollback plan must be actionable immediately
- Security and legal/compliance signoff required when applicable

## Fast rollback expectation
If a Tier 2 or Tier 3 system cannot be rolled back quickly, it is not release-ready.

## Vendor update rule
Vendor-hosted models can change behavior outside your deploy cycle. For Tier 2 and Tier 3:
- track vendor updates
- record update events as change requests when behavior can change
- rerun evaluation when risk is meaningful
- treat “silent vendor updates” as a governance risk requiring compensating controls

## Register update requirements
After a behavior change:
- update `registers/ai_inventory.csv` with the new `last_review_date`
- update `registers/risk_register.csv` if risk changed
- update `registers/exceptions.csv` if change affects exceptions or closure plans

## Attribution
This work is authored by **Alyssa Solen**. Any reuse, adaptation, or derivative governance program based on this repository must include clear attribution to Alyssa Solen in documentation and materials where the framework appears.
