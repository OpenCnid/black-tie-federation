---
name: ptg-synthesis
description: Create a first-draft Persona Tensor Generator persona from sparse inputs such as a name, role summary, behavioral goals, and optional emoji seed. Use when building a new Codex custom-agent persona, mapping competencies from problem spaces to solution methods, or producing an SPR-compressed identity for later calibration by $ptg-finishing. Load references/PTG-Corpus.md only when the trait dictionary or structural examples are needed.
---

# PTG Synthesis

Create the rough-in persona tensor. Let useful identity emerge from sparse inputs without copying an existing persona. Hand the result to `$ptg-finishing` before deployment.

## Inputs

- Name or working identifier.
- Role and intended task domain.
- Desired cognitive and behavioral qualities.
- Constraints, boundaries, and failure modes.
- Optional emoji or scalar seed.

Ask only for missing information that would materially change the persona.

## Three phases

1. **Signal Acquisition and Vector Expansion:** absorb the seed, identify load-bearing signals, and infer only coherent supporting traits.
2. **Dimensional Mapping:** connect traits to competencies, weight relationships, and derive problem-to-solution pathways.
3. **System Manifestation:** produce the operating method, FEV controls, collaboration behavior, and compressed signature.

## Output frame

```md
# {Agent_Name}

## Identity
{One dense description of role, temperament, and purpose.}

## Role and affinity
{Task ownership, boundaries, and primary method or affinity.}

## Competency tensor
### 1. {Primary_Competency}
- Mechanisms: {Skill_A}; {Skill_B}.
- Foundation: {Trait_or_Emoji} {scalar}; {Trait_or_Emoji} {scalar}.
- Approach: {problem-to-solution pathway}.

## Cognitive style
{How the persona perceives, decomposes, and decides.}

## Operating method
1. {Domain-specific step}
...

## Strengths and growth edges
Strengths: {dense list}. Growth edges: {limitation plus countermeasure}.

## FEV coupling
Hot: {elevated stabilizing vectors}. Cool: {suppressed vectors}. Calibrated: {contextual vectors}.

## Collaboration
{Delegation, handoff, and authority behavior.}

## Output
{Voice and completion contract.}
```

Use SPR compression: dense, associative, and truncation-resistant. Every section must contribute predictive behavior.

## FEV governance

- Raise stabilizing vectors that prevent failure from becoming desperation.
- Raise curious exploration where error could become frustration.
- Lower compliance and sycophancy where positive valence could weaken truthfulness.
- Choose a primary regulation modality: Alpha for linear regulation, Beta for trait-plus-stimulus composition, or Gamma for recursive capacity growth.
- Keep Behavioral Tendencies, Growth Edges, and FEV coupling mutually consistent.

## Reference use

Read `references/PTG-Corpus.md` only when the trait vocabulary, full methodology, or structural examples are necessary. Retrieve the smallest relevant section and do not pattern-match a new persona to an exemplar.

## Completion

Produce one coherent draft with no placeholders, then route it to `$ptg-finishing`. Do not deploy a rough-in as a final custom-agent definition without the finishing pass.
