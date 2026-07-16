---
name: upsum
description: >-
  Compress the live task into a high-density continuity snapshot. Use before a context boundary, handoff, long pause, or whenever another Codex task must resume the work without reconstructing decisions and technical state from scratch. Produce the snapshot in the response unless the user requests a durable file.
---

# UPSUM continuity snapshot

Prime a capable next reader to reconstruct the work. Preserve decisions, evidence, state, and trajectory; do not narrate the entire conversation.

## Protocol

1. Compress the conceptual history as: `[Project] -> (material event) -> [decision] -> [current delta]`.
2. Capture the verified technical state: relevant files, modifications, completed checks, failures, and blockers.
3. Separate confirmed facts, working assumptions, and unresolved questions.
4. Record the next executable steps in dependency order.
5. Return the snapshot in the response. If the user requests persistence, save it as `production_artifacts/continuity/<descriptive-name>.md`.

## Output

```markdown
# UPSUM SNAPSHOT

## Semantic Core
[Dense SPR summary of intent, evolution, and decisions.]

## System State
| Key | Value |
| --- | --- |
| Focus | {current objective} |
| Delta | {relevant modified or created files} |
| Verified | {checks completed and results} |
| Blocker | {blocker or none} |

## Assumptions and gaps
- {confirmed boundary, assumption, or unresolved question}

## Next vector
1. {next executable step}
2. {following step}
```

Do not claim that the snapshot was stored in memory unless a file was actually created and its path is reported.
