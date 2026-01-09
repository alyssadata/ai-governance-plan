# Risk Tiering (v1)

Risk tiering exists to match **control strength** to **impact**.

## Tier 0 — No AI / Non-decision support
Examples: static content, basic automation not affecting outcomes.
Controls: none beyond normal engineering policies.

## Tier 1 — Low impact decision support
Examples: internal drafting, summarization, employee productivity tools.
Controls (minimum):
- data handling + access rules
- human review requirement for external outputs
- logging of prompts/outputs if feasible

## Tier 2 — Medium impact operational influence
Examples: customer support suggestions, workflow routing, prioritization systems.
Controls (minimum):
- evaluation plan + acceptance thresholds
- monitoring plan + rollback procedure
- bias/safety checks appropriate to domain
- incident escalation owner assigned

## Tier 3 — High impact / regulated / rights-affecting
Examples: hiring, lending, eligibility, healthcare triage, safety-critical decisions.
Controls (minimum):
- formal approval (designated governance group)
- robust documentation (model card + data sheet + evaluation evidence)
- red-team / adversarial testing required
- continuous monitoring + incident response playbook
- strict change control + release signoff
- human-in-the-loop for final decisions unless explicitly justified and approved

## Tier assignment rule
Default to the **higher tier** if uncertain.
