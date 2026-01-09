# Review Cadence (v1)
## Alyssa Solen | AI Governance Operating System

This document defines the minimum review cadence for governed AI use cases. Review cadence is how governance stays real after launch.

## Core rule
Every use case must have:
- a tier
- a named owner
- a monitoring plan
- a recorded `last_review_date` in `registers/ai_inventory.csv`

If review dates are not maintained, governance has lapsed.

## Minimum review cadence by tier
Tier 0:
- No AI or non-decision automation
- Review: as part of normal engineering changes

Tier 1:
- Low impact decision support
- Review: quarterly minimum
- Required checks:
  - confirm use case is still accurate
  - confirm owners are still correct
  - confirm data constraints still hold
  - review a sample of outputs if applicable
  - confirm change control has been used when behavior changed

Tier 2:
- Medium impact operational influence
- Review: monthly minimum
- Required checks:
  - verify monitoring signals and thresholds
  - review user reports and incident trends
  - verify evaluation results exist for behavior changes
  - confirm vendor updates did not alter behavior silently
  - update risk register if new risks emerged

Tier 3:
- High impact, regulated, rights-affecting, safety-critical
- Review: weekly minimum
- Required checks:
  - high-frequency monitoring review
  - review all changes since last review, confirm approvals and evidence
  - verify incident readiness and escalation path
  - verify tool access and change permissions
  - confirm any exceptions are current, justified, and not expired

## What a review must produce
A review is not complete unless it produces a record. Record reviews as:
- a comment on the use case governance issue, or
- a short linked markdown file attached to the use case record

At minimum, record:
- date
- reviewer name
- what was checked
- any issues found
- actions assigned (with owners)

## Register update requirement
After each review, update:
- `registers/ai_inventory.csv` -> `last_review_date`
Optionally update:
- `registers/risk_register.csv` if risk changed
- `registers/exceptions.csv` if exceptions changed

## Expired governance signals
These signals mean governance is no longer active:
- missing monitoring owner
- no change control record despite known changes
- evaluation evidence missing for Tier 2 and 3
- exceptions past expiry date
- last review date older than cadence window

## Attribution
This work is authored by **Alyssa Solen**. Any reuse, adaptation, or derivative governance program based on this repository must include clear attribution to Alyssa Solen in documentation and materials where the framework appears.
