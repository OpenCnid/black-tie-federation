---
name: prompt-engineering
description: Design and refine prompts, reusable templates, custom-agent instructions, and output schemas through structural clarity rather than magic words. Use for semantic tagging, hierarchy, parameterized placeholders, collections, attention management, constraint precedence, and iterative prompt diagnosis. Pair with $hypershot-protocol when a structural example must prime form without contaminating content.
---

# Prompt Engineering

Use structural clarity and task alignment. Build only the control surface the model needs.

## Toolkit

### Semantic containers

Separate context, task, constraints, inputs, tools, and output instructions with clear headings or XML-style tags when boundaries matter.

### Hierarchy

Match structure to the problem:

- Numbered lists for sequence.
- Bullets for parallel requirements.
- Nested headings for domain decomposition.
- Tables for repeated fields and comparisons.

### Parameterized placeholders

Use consistent placeholders for reusable prompts:

- `${...}` for user-provided values.
- `{...}` for named objects, methods, or components.
- `[...]` for collections.
- `(...)` for options or decisions.

Define each placeholder once. Do not mix syntaxes without a reason.

### Collections

Represent repeated data explicitly as lists, key-value objects, tables, or schemas. Preserve field names across input and output when traceability matters.

### Attention and precedence

- Put the objective and highest-priority constraints near the beginning.
- Restate only truly load-bearing completion conditions near the end.
- Group related constraints.
- State precedence when instructions can conflict.
- Prefer positive behavioral instructions over long prohibition lists.

## Construction loop

1. Define the desired observable outcome.
2. Map the distance between the supplied context and that outcome.
3. Separate stable instructions from task-specific variables.
4. Add constraints only where a plausible failure mode requires them.
5. Define the output contract and completion condition.
6. Test against representative cases.
7. Locate divergence, revise at that point, and repeat.

## Structural template

```xml
<request type="${request_type}">
  <context>${context}</context>
  <task>${objective}</task>
  <inputs>${inputs}</inputs>
  <constraints>${constraints}</constraints>
  <output_instructions>
    Format: ${format}
    Audience: ${audience}
    Completion: ${completion_condition}
  </output_instructions>
</request>
```

Treat this as a hypershot: preserve the structure, then instantiate variables from the task. Do not copy example content into unrelated prompts.

## Quality checks

- Every instruction changes behavior or removes a material ambiguity.
- The prompt identifies the objective, inputs, constraints, and completion condition.
- Tools and authority are not implied when they are unavailable.
- Output requirements are testable.
- Private context appears only when necessary and authorized.
