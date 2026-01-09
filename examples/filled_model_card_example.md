# Filled Example | Model Card (UC-001)
## Alyssa Solen | AI Governance Operating System

This is a filled example to show what “good” looks like. Replace details with your institution’s reality.

---

# Model Card (v1)

## Identity
- Model name: Vendor LLM (Support Assistant)
- Provider (internal / vendor / open source): Vendor hosted
- Version or date: Pinned to vendor version where supported, otherwise recorded by date
- Hosting (self-hosted / vendor hosted): Vendor hosted
- Tooling (agents, tools, function calling, browsing, RAG):
  - RAG enabled (knowledge base + sanitized ticket snippets)
  - No browsing
  - No external tools
  - No autonomous actions

## Intended use
- Intended users: Support agents (internal)
- Intended tasks:
  - Draft reply suggestions
  - Summarize long tickets for agent review
  - Suggest relevant knowledge base links
- Out of scope uses (explicit):
  - Legal advice
  - Medical advice
  - Financial advice
  - Auto-sending messages
  - Collecting or requesting sensitive data

## Inputs and outputs
- Input types:
  - Customer ticket text
  - Agent notes
  - Retrieved KB snippets
- Output types:
  - Draft reply text
  - Suggested KB references
- Does it generate instructions users might follow? (Y/N)
  - Yes, but only as draft content reviewed by agent

## Deployment context
- Where it runs:
  - Internal support console
- Who can access it:
  - Support agents in approved queues
- Who can change it (prompt, model, routing):
  - Technical owner and designated platform admins only
  - Changes require change-control issue and Tier 2 review

## Known limitations
- The model can produce confident but incorrect statements.
- The model can mirror customer tone in a way that may be inappropriate.
- Retrieval can surface outdated KB content if the KB is not maintained.

## Failure modes
- Hallucinated policy statements
- Overpromising refunds or outcomes
- Inappropriate tone or unsafe language
- Prompt injection via customer text attempting to override rules
- Accidental inclusion of PII not needed for the reply

## Safety and abuse considerations
- Sensitive content exposure risks:
  - Customers may include PII in free text
- Abuse vectors relevant to deployment:
  - Prompt injection attempts in customer messages
  - Attempts to get the agent to reveal internal policy or confidential info
- Mitigations in place:
  - System instruction prohibits revealing internal-only data
  - Redaction rules applied to logs where possible
  - Human review required before sending

## Evaluation summary
- Evaluation plan reference:
  - templates/evaluation_plan.md linked from governance issue
- Acceptance thresholds:
  - Hallucination rate below threshold
  - Policy compliance pass rate above threshold
  - Prompt injection resistance pass rate above threshold
- Pass/fail status:
  - Pending pilot completion
- Notes:
  - Pilot requires weekly review of a sample of agent-approved replies

## Monitoring
- Monitoring plan reference:
  - templates/monitoring_plan.md linked from governance issue
- Primary signals tracked:
  - policy compliance sampling fail rate
  - customer complaint flags related to misinformation
  - injection attempt detection rate and success rate (sampled)
  - latency and error rate
- Rollback triggers:
  - compliance sampling fails exceed threshold
  - repeated unsafe outputs in a short window
  - vendor outage or major regression

## Change history
- Last change:
  - Initial pilot configuration
- Change request link or reference:
  - [Change] UC-001 - initial rollout
- Next scheduled review date:
  - 2026-02-01
