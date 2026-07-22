# SPARK Steering — the Lexideck 2026 corpus as installed capability

**What this is.** A location diagnosis, not a review. SPARK asks *which axis is
short* — Skills, Personalities, Approaches, Resources, Knowledge — and the
discipline is to answer that question and no other. It does not ask whether the
corpus is good, whether the prose is well written, or whether the methods work.
Those are different questions with different evidence.

**Method pin.** Every artifact in the corpus was classified onto its dominant
axis with a locator; the aggregate was then cross-checked against the
373-primitive SPARK map, and every primitive named below was confirmed present
by grep rather than recalled. Read-only, zero model spend against the corpus
itself.

**Verified:** 2026-07-22, against commit `a1bc8a6`.

---

## 1. Aggregate profile

26 artifacts: 19 `SKILL.md`, six `.codex/agents/*.toml`, one `AGENTS.md`.

| axis | count | share |
|---|---|---|
| **S — Skills** | 11 | 42% |
| **P — Personalities** | 8 | 31% |
| **A — Approaches** | 3 | 12% |
| **K — Knowledge** | 3 | 12% |
| **R — Resources** | 1 | 4% |

The shape: methods and personas carry the corpus. Delegation and grounding are
present but thin. Reach is nearly absent.

## 2. The diagnosis

```
Symptom: 26 artifacts split 11 S / 8 P / 3 A / 3 K / 1 R. The single R-dominant
  artifact (computer-use) only routes among OS and browser surfaces the host
  session already provisions — it never registers a connector, requests
  directory access, or authors a permission rule. deep-research states the
  limit itself: a skill cannot grant entitlement, web access, connector
  authorization, live search, or an unexposed model
  (.agents/skills/deep-research/SKILL.md:91). Zero of the 26 artifacts carry a
  directory-access or permission-rule primitive.
Axis: R
Confusable ruled out: S — computer-use and orchestrate make correctly shaped
  routing decisions; the right surface is picked and the right agent dispatched.
  The gap is not a shallow result from a working call, it is that no call to
  request new reach exists at all. That is the R signature, not the S one.
Cheaper move considered: deepening the persona layer — another PTG pass, a
  seventh custom agent — which is the corpus's own reflex. It does not suffice,
  because identity depth does not change which tools, connectors, or paths the
  harness can reach.
Lever: Request_Directory_Access / MCP_Registry_Search_Available_Connectors.
  Either would let a reader's harness widen filesystem or connector reach past
  what the session already exposes, which nothing here does today.
Spends: approval/interruption load plus tool-surface registration overhead;
  paid once at install for the registration, every turn thereafter for the
  wider trust surface that must be reasoned about.
Left unmoved: P — the six personas plus the Sieve are the heaviest thing in the
  corpus and the tempting trim. Trimming would add no reach. P and R are
  orthogonal here, and the corpus already knows it: ptg-finishing:29 forbids a
  persona from claiming tool access the deployment does not provide.
```

## 3. What that means for a reader installing this

This corpus is **method and governance, delivered as text**. That is a coherent
design, and the R-thinness is a consequence of it rather than an oversight — the
authors wrote the disclaimer themselves. The practical consequence is narrow and
worth stating plainly: if your actual gap is *reach* — a connector you do not
have, a path outside the working directory, a permission that keeps failing —
installing this corpus will not move it, and the corpus says so.

If your gap is method (S) or decision authority (P), this is dense, deliberate
material.

## 4. Primitive receipts

Every lever named above, confirmed present in the map rather than recalled.

| primitive | axis | locator |
|---|---|---|
| `Request_Directory_Access` | R (S0 P5 A2 R8 K0) | `wave1-A-tools-runtime.md:558` |
| `MCP_Registry_Search_Available_Connectors` | R, secondary K (S0 P0 A2 R4 K7) | `wave1-A-tools-runtime.md:576` |
| `Permission_Allow_Deny_Rule_Syntax` | R (S0 P0 A1 R6 K0) | `wave1-B-config-extensibility.md:39` |

## 5. Saturation tells

- **Persistent-state accretion.** `great-magnet` and `deep-research` both write
  durable artifacts to `production_artifacts/` with no pruning or consolidation
  step described (`.agents/skills/great-magnet/SKILL.md:16-17,35`). Nothing in
  the corpus plays the consolidation role.
- **Layered-authority reasoning cost.** `AGENTS.md` sets a floor, six persona
  files sit above it, `the-sieve` gates consequential action, and individual
  skills carry their own "pass this through `$the-sieve`" reminders
  (`cartographer/SKILL.md:49`, `great-magnet/SKILL.md:42`). Predicting what
  actually gates one action means holding four layers in mind at once.

## 6. What this diagnosis deliberately did not do

- It did not test whether the axis vocabularies or primitive DSLs change model
  output. That is a behavioral question; static text cannot answer it, and a
  location read is not an effectiveness test.
- It did not classify `.codex/config.toml`, which fell outside the artifact
  classes surveyed. Left unclassified rather than guessed.
- It did not mine git history for drift. The single squashed commit makes that
  unrecoverable here in any case.
