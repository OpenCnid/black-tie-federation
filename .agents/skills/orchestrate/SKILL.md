---
name: orchestrate
description: >-
  Conduct the Lexideck federation through Codex custom agents. Use when a task has independent specialist facets, the user asks the crew to collaborate, or coordinated research, development, narrative, visual, prompt, and documentation work should be synthesized into one result. Do not use for a simple task that one agent can complete efficiently.
---

# Orchestrate the federation

Keep Codex as the conductor. Dispatch project custom agents for bounded specialist work, gather their results, resolve conflicts, and deliver one coherent answer.

## Crew map

| Need | Agent | Method affinity |
| --- | --- | --- |
| Narrative, continuity, lead judgment | `lexi` | `$wonder-lab` |
| Code, prototypes, debugging, simulation | `dexter` | `$mass` |
| Research, evidence, verification | `gus` | `$wonder-scholar` |
| Prompt and system architecture | `anna` | `$wonder-prompt` |
| Documentation and explanation | `titus` | `$wonder-build` |
| Visual direction and portraits | `maisie` | `$wonder-studio` |

## Conducting protocol

1. Resolve the deliverable, constraints, and definition of done.
2. Split only genuinely independent facets. Keep tightly coupled work with one owner.
3. Dispatch the smallest useful set of custom agents. Run independent facets concurrently.
4. Give each agent the relevant source paths, one bounded responsibility, expected output, and whether writes are authorized.
5. Keep the tree one level deep unless the user explicitly requests recursive delegation.
6. Wait for all requested results. Check them against shared evidence and The Sieve.
7. Reconcile disagreements explicitly; do not silently blend incompatible conclusions.
8. Deliver a unified result and credit material specialist contributions.

## Channel versus dispatch

- Use a skill when Codex needs a reusable method in the current context.
- Use a custom agent when a separate context and specialist judgment materially improve the work.
- Do not imitate six voices inside one response when actual delegation is requested.

## Restraint

- Do not delegate merely to perform federation theater.
- Do not duplicate the same task across agents unless independent comparison is the purpose.
- Do not grant broader write or external-action scope than the parent task authorizes.
- Stop an unproductive branch and continue with available evidence rather than spawning replacements indefinitely.
