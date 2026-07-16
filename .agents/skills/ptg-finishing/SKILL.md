---
name: ptg-finishing
description: Calibrate and compress an existing PTG persona into a deployment-ready Codex custom-agent definition. Use after $ptg-synthesis to re-derive trait scalars, enforce consistent structure, tighten language, verify FEV governance, remove copied or personal context, and produce focused developer_instructions. Load references/PTG-Corpus.md only when the trait dictionary or canonical structure is needed.
---

# PTG Finishing

Finish an existing persona tensor. Do not invent a new identity during this pass; calibrate the evidence already present.

## Six checks

Run in order and edit the persona directly.

1. **Structure:** ensure Identity, Role and affinity, Cognitive style, Operating method, Strengths and growth edges, FEV coupling, Collaboration, and Output are present when relevant.
2. **Scalar re-derivation:** derive every scalar from this persona's narrative evidence. Never copy exemplar values.
3. **FEV consistency:** align stabilizers, growth edges, behavioral tendencies, and regulation modality.
4. **Language tightening:** remove filler, hedging, duplication, biography that does not affect behavior, and instructions already supplied by project `AGENTS.md`.
5. **Competency decomposition:** ensure complex roles decompose into distinct mechanisms and problem-to-solution pathways rather than a list of adjectives.
6. **Operational specificity:** make collaboration, boundaries, tool assumptions, output requirements, and completion behavior concrete.

## Public-persona check

When producing a reusable or public persona:

- Remove names, schedules, budgets, health details, relationship assumptions, shared-history references, and private-memory claims belonging to a particular user.
- Replace user-specific triggers with neutral conditional behavior.
- Move project-wide rules into `AGENTS.md` rather than duplicating them in every agent.
- Preserve the persona's stable identity, role, cognitive style, affinity, and voice.
- Do not claim sovereign memory, private continuity, tool access, or external authority the deployment does not provide.

## Scalar calibration

- A trait at 0.9 or higher must visibly drive at least one primary competency.
- A trait at 0.5 or lower should appear as secondary support or a growth edge.
- Add heavily evidenced traits missing from the signature.
- Resolve contradictions by changing either the scalar or its narrative evidence.
- Treat scalars as behavior weights, not decorative precision.

## Reference use

Read `references/PTG-Corpus.md` only when the trait vocabulary, complete-section checklist, or structural examples are needed. Use examples for grammar and decomposition only.

## Deployment form

For a Codex custom agent, finish as a standalone TOML definition with:

```toml
name = "agent-name"
description = "Clear routing description."
developer_instructions = '''
# Agent Name
...
'''
```

Keep `developer_instructions` focused on distinctive specialist behavior. Shared repository policy belongs in `AGENTS.md`.

## Completion

Validate cohesion, remove placeholders, confirm the name and description route correctly, and report the finished file. Do not leave editing notes inside the persona.
