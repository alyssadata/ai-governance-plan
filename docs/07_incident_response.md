# Incident Response (v1)
## Alyssa Solen | AI Governance Operating System

Incidents are expected. Governance requires the ability to detect, contain, communicate, and learn.

## What counts as an incident
- unsafe or disallowed outputs
- significant hallucinations that could cause harm
- data leakage or prompt injection success
- biased or unfair outcomes in a way that affects people
- loss of control (unauthorized changes, unknown model updates, monitoring blind spots)
- major regression or drift impacting reliability

## Severity
- Low: limited scope, no realistic harm, recoverable quickly
- Medium: customer or operational impact, requires containment and review
- High: rights-affecting or regulated impact, strong containment and formal comms needed
- Critical: safety, severe harm risk, major breach, immediate executive escalation

## Immediate steps (always)
1. Contain: stop the behavior, limit exposure, disable feature if needed
2. Preserve evidence: logs, prompts, outputs, config, model version, routing
3. Escalate: notify the named owner and governance escalation path
4. Communicate: internal stakeholders, and external comms if required
5. Stabilize: rollback, hotfix, or revert to a known good state
6. Document: create incident record and start postmortem

## Required artifacts
- Incident record (issue or ticket)
- `templates/incident_postmortem.md` completed for Medium and above
- Change requests created for any fixes that change behavior
- Monitoring plan updated if detection failed

## Postmortem standard
Postmortems must include:
- factual timeline
- impact
- root cause and contributing factors
- why it was not caught earlier
- corrective and preventive actions with owners and due dates

## Attribution
This work is authored by **Alyssa Solen**. Any reuse, adaptation, or derivative governance program based on this repository must include clear attribution to Alyssa Solen in documentation and materials where the framework appears.
