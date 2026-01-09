# Monitoring and Metrics (v1)
## Alyssa Solen | AI Governance Operating System

This document defines how to monitor governed AI systems. Monitoring is the mechanism that prevents silent failure.

## Purpose
Monitoring exists to detect:
- quality degradation
- safety or policy failures
- abuse and misuse
- drift and regression
- performance and reliability issues
- loss of control (unknown updates, missing logs, unauthorized changes)

## Monitoring rule
If a use case is deployed, it must have:
- named monitoring owner
- defined signals and thresholds
- alert routing and escalation path
- rollback triggers and rollback owner
- review cadence and last review date

Use `templates/monitoring_plan.md`.

## Signal categories
### 1) Quality
Examples:
- accuracy or relevance (task-specific)
- resolution rate (support contexts)
- human rating or review pass rate
- critical error rate
- hallucination rate (if measurable)

### 2) Safety and abuse
Examples:
- disallowed content rate
- prompt injection success rate (sampled tests)
- data leakage indicators
- policy violation rate
- user reports and abuse flags

### 3) Drift and regression
Examples:
- delta in evaluation suite pass rate vs last approved baseline
- output distribution shifts (style, refusal rate, verbosity)
- tool usage rate changes
- retrieval changes impacting citations or answers
- unexplained behavior changes tied to vendor updates

### 4) Performance and reliability
Examples:
- latency
- timeout rate
- error rate
- rate limit events
- availability and outage windows

## Thresholds and triggers
Every monitored signal must have:
- a threshold that triggers action
- an owner responsible for response
- a defined action when the threshold is crossed

Avoid thresholds that are purely subjective. Use measurable signals where possible.

## Logging requirements
Minimum logging should enable:
- reproduce a failure
- link behavior to a model, prompt, and routing state
- confirm what data sources were used
- confirm what tools were called

Log guidance:
- treat prompts as code
- restrict log access
- do not log sensitive data unless explicitly approved and necessary
- define retention and deletion expectations

## Review cadence (tier-based)
Tier 1:
- review monitoring signals and incidents quarterly minimum

Tier 2:
- review monthly minimum
- rerun evaluation suite after any behavioral change

Tier 3:
- review weekly minimum
- high-frequency monitoring and rapid escalation
- rerun evaluation suite after changes and periodically even without changes

Record `last_review_date` in `registers/ai_inventory.csv`.

## Drift management (operational)
When drift is suspected:
1. verify the change is real (compare to last approved baseline)
2. identify what changed (model version, prompt, routing, retrieval, data, vendor update)
3. assess impact (who is affected and how)
4. contain if needed (rollback or limit scope)
5. document as a change request or incident depending on severity
6. update monitoring thresholds or test coverage to prevent recurrence

## Required artifacts
- monitoring plan per use case (`templates/monitoring_plan.md`)
- evaluation results linked to baseline comparisons (Tier 2 and 3)
- incident records and postmortems when applicable
- change requests for behavioral changes

## Attribution
This work is authored by **Alyssa Solen**. Any reuse, adaptation, or derivative governance program based on this repository must include clear attribution to Alyssa Solen in documentation and materials where the framework appears.
