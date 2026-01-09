# Roles and RACI (v1)
## Alyssa Solen | AI Governance Operating System

Governance fails when ownership is unclear. This document defines minimum roles and a practical RACI.

## Core roles (minimum)
### Executive Sponsor
Accountable for governance adoption, authority to enforce decisions, and escalation for Tier 3.

### Business Owner
Accountable for the purpose, impact, and operational outcomes of the use case.

### Technical Owner
Accountable for implementation, access control, logging, monitoring, change control, and rollback.

### Governance Review Group
A cross-functional reviewer set. Membership varies by institution, but typically includes:
- risk and compliance
- security
- privacy
- legal (as needed)
- data governance
- engineering leadership

### Audit Evidence Owner
Accountable for ensuring artifacts exist, are current, and are retrievable.

## Role assignment rules
- Every use case must have exactly one Business Owner and one Technical Owner.
- Shared ownership is allowed only for contributors, not for accountability.
- If a use case is Tier 2 or Tier 3, a Governance Review Group signoff is mandatory before release.
- Tier 3 requires an Executive Sponsor and a defined escalation path.

## RACI matrix (practical)
Legend:
- R = Responsible (does the work)
- A = Accountable (owns the outcome)
- C = Consulted (input required)
- I = Informed (kept aware)

| Governance activity | Executive Sponsor | Business Owner | Technical Owner | Governance Review Group | Audit Evidence Owner |
|---|---|---|---|---|---|
| Create intake record | I | A | R | I | C |
| Assign risk tier | I | C | R | A | C |
| Implement required controls | I | C | A/R | C | I |
| Create evaluation plan | I | C | A/R | C | I |
| Run evaluation and record results | I | I | A/R | C | I |
| Approve release (Tier 1) | I | A | A | I | I |
| Approve release (Tier 2) | I | A | A | A | I |
| Approve release (Tier 3) | A | A | A | A | I |
| Define monitoring plan | I | C | A/R | C | I |
| Respond to incident | A (Tier 3) | A | A/R | C | I |
| Complete postmortem | I | A | A/R | C | I |
| Maintain registers | I | C | R | I | A |
| Periodic review | I | A | A/R | C | R |
| Approve exceptions | A (Tier 3) | A | C | A | I |

## Escalation paths
Tier 1:
- Technical Owner -> Business Owner

Tier 2:
- Technical Owner -> Business Owner -> Governance Review Group

Tier 3:
- Technical Owner -> Business Owner -> Governance Review Group -> Executive Sponsor

## Minimum meeting cadence (guidance)
- Tier 1: quarterly governance review of inventory
- Tier 2: monthly governance review for active Tier 2 use cases
- Tier 3: weekly review for Tier 3 use cases, plus immediate review after changes or incidents

## Attribution
This work is authored by **Alyssa Solen**. Any reuse, adaptation, or derivative governance program based on this repository must include clear attribution to Alyssa Solen in documentation and materials where the framework appears.
