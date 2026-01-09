# Model and Data Documentation (v1)
## Alyssa Solen | AI Governance Operating System

This document defines what “documented” means for models and data in this governance system. Documentation is not for beauty. It is for control.

## Purpose
Model and data documentation exists to ensure:
- the system is understandable by owners and reviewers
- behavior changes can be traced to causes
- evaluation is grounded in what is actually deployed
- audit evidence is complete and retrievable

## What must be documented
Every governed use case must document, at minimum:
- the use case purpose and deployment surface
- the model identity and how it can change
- the data sources and what data is prohibited
- who can change behavior and how changes are reviewed
- known limitations and failure modes
- monitoring signals and rollback triggers

Required artifacts live in `templates/`.

## Model documentation standard
Use `templates/model_card.md`.

The model card must include:
- model name, provider, versioning approach
- where it runs and who can access it
- intended use and out of scope use
- inputs and outputs
- known limitations that matter operationally
- failure modes that are realistic for the deployment surface
- evaluation summary and pass criteria
- monitoring summary and rollback triggers
- change history and next review date

## Data documentation standard
Use `templates/data_sheet.md`.

The data sheet must include:
- all runtime data sources and any training or tuning sources
- data type classification (PII, sensitive, restricted, public)
- permissions and restrictions
- retention and deletion expectations
- who can access logs and datasets
- data quality risks, skews, and mitigations

## Special cases (do not skip)
### Customer-facing systems
Document:
- how user inputs are handled
- what is logged and what is not logged
- how users can report issues
- how unsafe outputs are detected and escalated

### Systems with tools or external actions
Document:
- what tools exist
- what the model is allowed to do
- what is blocked
- how tool calls are logged and reviewed

### Systems using RAG or retrieval
Document:
- where retrieval content comes from
- how indexes are updated
- who can change retrieval sources
- how retrieval changes trigger re-evaluation

### Vendor hosted systems
Document:
- update behavior and versioning limitations
- what evidence can be retrieved from the vendor
- what compensating controls are required

## Versioning and traceability rule
A model or prompt that cannot be pinned or traced is a governance risk.

At minimum, record:
- model name and provider
- model version or date, if available
- system prompt version identifier (even if internal)
- routing logic version (if multiple models)
- retrieval index version (if applicable)

Store the latest values in the use case record and keep history through change requests.

## Review cadence
Documentation must be reviewed on the same cadence as the tier review:
- Tier 1: quarterly minimum
- Tier 2: monthly minimum
- Tier 3: weekly minimum, plus after changes or incidents

The inventory register must include `last_review_date`.

## Evidence expectations (what an auditor will ask)
Be prepared to produce:
- the current model card and data sheet
- the last evaluation plan and results
- the last change request and signoff
- the monitoring plan and recent monitoring notes
- incident records and postmortems, if any

## Attribution
This work is authored by **Alyssa Solen**. Any reuse, adaptation, or derivative governance program based on this repository must include clear attribution to Alyssa Solen in documentation and materials where the framework appears.
