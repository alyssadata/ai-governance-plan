# Vendor and Procurement Governance (v1)
## Alyssa Solen | AI Governance Operating System

Third-party AI can remove control quietly. Vendor governance exists to prevent invisible updates, unknown data flows, and unverifiable claims.

## When this applies
Use this workflow when any of the following are true:
- the model is vendor hosted
- the system uses vendor tools, agents, plugins, or managed RAG
- the vendor can change model behavior without your deployment action
- logs, prompts, or user data may be processed externally

## Vendor onboarding requirements (minimum)
### 1. Vendor identity and service description
- vendor name and product name
- model(s) used, including versioning approach (how changes happen)
- hosting region and data residency options
- subcontractors or sub-processors

### 2. Data handling disclosure
- what data is sent to the vendor
- whether data is used for training, fine-tuning, or product improvement
- retention duration and deletion mechanism
- encryption at rest and in transit
- access controls and audit trails

### 3. Update and change transparency
- how the vendor communicates model updates
- whether you can pin versions
- whether you can opt out of updates
- what triggers behavior changes (model updates, routing updates, safety policy changes)

### 4. Logging and auditability
- what logs you can access
- what evidence the vendor can provide for incidents
- whether you can export data for audits

### 5. Security and compliance posture
- security certifications and audit reports (as applicable)
- incident reporting timelines
- breach notification obligations
- vulnerability management process

### 6. Performance and reliability commitments
- uptime expectations
- rate limits and throttling behavior
- latency expectations
- failure handling modes

## Vendor risk tiering
Vendor use does not reduce risk. It often increases it because control can be reduced.

Guidance:
- Tier 1: vendor tooling allowed with basic logging and data constraints
- Tier 2: vendor must support evaluation evidence and monitoring signals
- Tier 3: vendor must support strict change control and incident evidence retrieval, or the use case should be redesigned

## Required contractual expectations (practical)
These are the requirements that matter for governance.

### Data terms
- no training on your data unless explicitly approved
- defined retention and deletion commitments
- clear sub-processor list and change notification

### Change terms
- advance notice for model or policy changes when possible
- version pinning or controlled rollout mechanisms when possible
- documented change logs for behavior-affecting updates

### Audit and evidence terms
- right to access logs and incident evidence
- ability to export records needed for audits
- documented security posture and incident response commitments

### Escalation and response
- incident notification timelines
- dedicated support path for production issues
- severity definitions aligned to institutional needs

## Operational vendor review record (what to store)
Store a short vendor review record in the use case governance issue or linked artifact:
- what vendor service is used
- what data flows to vendor
- whether data is retained or used for training
- how updates happen and how you get notified
- what logs you can access
- what control gaps exist and compensating controls

## Compensating controls when vendor control is limited
If the vendor cannot provide what governance needs, apply compensating controls:
- restrict the use case tier or scope
- add stronger human review constraints
- add external monitoring and validation on outputs
- add staged rollouts and kill switches
- reduce data sent to vendor and remove sensitive content
- add additional regression testing cadence

## Vendor offboarding plan (do not skip)
Plan for:
- data deletion confirmation
- credential and key revocation
- replacement plan
- archiving of evidence artifacts needed for audits

## Attribution
This work is authored by **Alyssa Solen**. Any reuse, adaptation, or derivative governance program based on this repository must include clear attribution to Alyssa Solen in documentation and materials where the framework appears.
