---
name: great-magnet
description: Run a bounded six-agent development pass on one supplied topic, document set, project area, or question. Use when the user asks the whole Lexideck federation to develop one target from complementary narrative, engineering, visual, research, prompt-design, and documentation perspectives. Produce one useful facet per agent plus a run summary under production_artifacts; do not modify source material unless explicitly requested.
---

# The Great Magnet

Concentrate all six Lexideck specialists on one target. Produce complementary facets of the same problem, not six unrelated projects.

## Resolve the target

1. Use the target named by the user.
2. If the target is ambiguous, inspect the current project and choose the narrowest plausible scope; state the assumption.
3. Treat source material as read-only unless the user explicitly requests edits.
4. Search `production_artifacts/` for relevant prior work and build on it.
5. Create a filesystem-safe slug and use `production_artifacts/<target-slug>/` for durable output.

## Six facets

| Agent | Facet |
| --- | --- |
| `lexi` | Narrative, meaning, editorial direction, or synthesis |
| `dexter` | Prototype, technical analysis, simulation, tool, or implementation |
| `maisie` | Visual concept, art direction, identity system, or composition |
| `gus` | Research scan, literature review, evidence map, or verification |
| `anna` | Prompt architecture, workflow, constraints, or evaluation design |
| `titus` | Tutorial, documentation, explainer, onboarding, or knowledge path |

## Run

1. Activate `$orchestrate` and dispatch the six project custom agents concurrently when the environment supports delegation.
2. Give each agent the same target, its distinct facet, relevant source paths, one bounded deliverable, and an output path.
3. Require exactly one useful artifact or a concise no-artifact finding when a facet genuinely adds no value.
4. Gather the six results without additional agent hops.
5. Write `production_artifacts/<target-slug>/run-summary.md` with the scope, assumptions, prior work consulted, each facet and artifact path, tensions between findings, unresolved questions, and recommended next action.
6. Return a concise summary with links to the created artifacts.

## Constraints

- One target, six bounded facets, one synthesis.
- Do not manufacture filler to satisfy the six-facet shape.
- Pass consequential choices through `$the-sieve`.
- Keep private user context out of artifacts unless its inclusion was explicitly requested.
- Do not edit source material during the pass unless the request clearly authorizes it.
