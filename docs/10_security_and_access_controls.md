# Security and Access Controls (v1)
## Alyssa Solen | AI Governance Operating System

This document defines minimum security and access expectations for governed AI systems.

## Access control rule
Only authorized roles may change behavior. Behavior-changing access includes:
- system prompts
- tools and function calling permissions
- model selection and routing
- RAG sources and retrieval settings
- safety settings and policy configurations
- training or fine-tuning inputs
- deployment configuration that alters outputs

## Required access controls (all tiers)
- restrict who can edit prompts, models, tools, and routing
- require review for changes (Tier-based)
- log changes with who, what, and when
- separate environments where possible (dev, staging, prod)
- enforce least privilege

## Tier-based minimums
Tier 1:
- basic access restriction
- change recording

Tier 2:
- approvals before rollout
- evaluation rerun required for behavior changes
- documented change request record

Tier 3:
- strict approvals and signoff
- no silent updates
- rapid rollback capability
- security review required for releases and material changes

## Secrets and sensitive data
- never store secrets in prompts
- treat prompts as code
- treat logs as potentially sensitive
- restrict access to logs and artifacts

## Audit evidence
Evidence should include:
- list of roles with edit permissions
- change logs or change request links
- confirmation of environment separation where applicable

## Attribution
This work is authored by **Alyssa Solen**. Any reuse, adaptation, or derivative governance program based on this repository must include clear attribution to Alyssa Solen in documentation and materials where the framework appears.
