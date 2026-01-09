# Filled Example | Use Case Intake (UC-001)
## Alyssa Solen | AI Governance Operating System

This is a filled example to show what “good” looks like. Replace details with your institution’s reality.

---

# AI Use Case Intake

## Summary
- Use case name: Support Reply Assistant
- Business owner: Customer Support Operations Lead
- Technical owner: Platform Engineering Lead
- Intended users: Support agents (internal)
- Deployment surface (internal tool / customer-facing / API / embedded): Internal support console

## Purpose
- What problem does it solve?
  - Helps agents draft faster, more consistent replies with fewer escalations.
- What decision or action does it influence?
  - Influences agent responses. Does not auto-send messages. Human review required.

## System description
- Model(s) used (vendor / open / internal):
  - Vendor-hosted LLM (version pinned where possible)
- Data sources used:
  - Knowledge base articles (approved content)
  - Prior resolved ticket snippets (sanitized)
- Does it use personal data? (Y/N)
  - Yes (tickets may include PII)
- Does it use sensitive data? (Y/N)
  - No (sensitive categories prohibited, redaction enforced)
- Does it affect rights/eligibility/safety? (Y/N)
  - No

## Risk indicators (check all that apply)
- [x] Customer-facing
- [ ] Automated action (not only suggestion)
- [ ] Regulated domain
- [ ] Vulnerable population
- [ ] Safety-critical
- [ ] Produces legal/financial/medical guidance
- [x] Uses PII
- [ ] Uses sensitive attributes

## Proposed tier (T0/T1/T2/T3) + rationale
- Tier: T2
- Rationale:
  - Customer-facing content is produced.
  - Uses PII in ticket context.
  - Human review remains in loop, but quality and safety failures can still impact customers.

## Required controls (link to docs/04_controls_catalog.md)
- Controls to implement:
  - A2 Governance review required
  - C2 Data sheet required (PII handling, retention, access)
  - E2 Evaluation plan and thresholds
  - F1 Abuse and misuse checks (prompt injection attempts via customer text)
  - G2 Monitoring plan with thresholds
  - H2 Rollback plan
- Evidence artifacts to produce:
  - Model card, data sheet, evaluation plan and results, monitoring plan, release checklist

## Rollout plan
- Pilot scope:
  - 10 agents, 2 support queues, 2 weeks
- Human review plan:
  - Agent must approve before sending. No auto-send.
- Monitoring owner:
  - Support Systems Engineer
- Rollback plan (1-2 sentences):
  - Disable assistant feature flag immediately if safety threshold triggers or reply error rate spikes beyond limit.

## Signoff
- Governance approval: Pending
- Security approval: Required (PII and vendor-hosted)
- Legal/compliance approval (if required): Not required for this scope
- Date: 2026-01-09

