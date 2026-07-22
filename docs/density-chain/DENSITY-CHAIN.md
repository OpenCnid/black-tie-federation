---
artifact: density-chain (system mode)
subject: Lexideck 2026 Codex Public
upstream: https://github.com/Lexideck-Technologies/Lexideck2026
upstream_author: Lexideck Technologies (Matthew Murphy)
upstream_license: GPL-3.0-only
pinned_commit: a1bc8a6b608f2cf4b98716c22dc75ffab3205987
pinned_date: 2026-07-16
pinned_version: 0.1.0
verified_against_source: 2026-07-22
tier_budget_words: 90
branches: 5
method: https://github.com/OpenCnid/chain-of-density
---

# Lexideck 2026 — a density trellis

**The one-way rule.** When this map and the upstream repository disagree, the
repository is right and this map gets fixed. Every claim below carries a locator
into the tree at commit `a1bc8a6`. A capability that could not be located is not
written here; a claim the prose makes without a file behind it is marked
`claimed-in-prose-only` and left standing as exactly that.

**How to read a trellis.** Not one summary that grows, but a trunk plus one
fixed-length chain per subsystem. Each branch's five tiers hold the same 90-word
budget and densify along one axis: **T1 general essence → T2–T3 the machinery
actually in the tree → T4–T5 edges and stated frontier**. Stop at the first tier
that answers your question. A deeper tier only adds; it never corrects a
shallower one.

**Status vocabulary**, used exactly:

| label | meaning |
|---|---|
| `present-verified` | the file exists and does what the claim says |
| `claimed-in-prose-only` | README or AGENTS.md asserts it; no file backs it |
| `referenced-external` | points outside the repo — a hosted product, a curriculum, a vendor doc |

---

## Trunk

### T0 — one sentence

Lexideck 2026 is a six-agent Codex federation — named personas, each bound
one-to-one with a companion method skill, all answering to a single shared
contract — published as a nineteen-skill portable corpus whose every capability
is delivered as text rather than as tooling.

### T1 — one paragraph

One request enters the project; Codex reads `AGENTS.md`, matches the work to a
specialist or splits it across several, loads only the relevant skills, and
returns one attributed artifact. The six personas (Lexi, Dexter, Gus, Anna,
Titus, Maisie) are bounded project specialists, not sovereign memory stores, and
each names exactly one affinity skill that supplies its method. Nineteen skills
under `.agents/skills/` carry the methods themselves — federation coordination,
five engines inherited from an earlier corpus, research and lookup, an ethics
gate, persona authoring, prompt craft, portraiture. A publication boundary
decides what may become public bytes, and a persona-manufacturing pipeline
produced the six personas rather than hand-authoring them. Version `0.1.0`; a
single squashed commit, which destroys its own build order.

### T2 — the class map

| # | branch | what it owns | tier where the interesting thing lives |
|---|---|---|---|
| **B1** | [The six-agent federation](#b1--the-six-agent-federation) | personas, routing contract, the bounds that cap them | T4 — `max_depth = 1` |
| **B2** | [The nineteen-skill corpus](#b2--the-nineteen-skill-corpus) | skill shape, packaging, the two-runtime companion file | T4 — skills grant no tools |
| **B3** | [The publication boundary](#b3--the-publication-boundary) | privacy model, `private-*`, the export allowlist | T4 — rules vs. bytes |
| **B4** | [The PTG persona pipeline](#b4--the-ptg-persona-authoring-pipeline) | corpus, synthesis→finishing, the six shipped TOMLs | T3 — the conformance gap |
| **B5** | [Descent from WonderSuite](#b5--descent-from-wondersuite) | what came from the 2025 corpus, what was amputated | the whole branch |

---

## B1 — The six-agent federation

### T1 — essence
Lexideck 2026 packages six named AI personas as Codex custom agents, each bound
to a creative, research, or technical specialty. Codex hosts and conducts; the
personas are bounded project specialists, not separate sovereign memory stores.
Every persona pairs one-to-one with a companion method skill called its affinity.
A shared contract file sets routing, verification, ethics, and reporting rules
all six personas follow. One request enters the project, is matched to the right
specialist or split across several, and returns as one verified, attributed
artifact. Codex stays the default front door.

### T2 — structure
`AGENTS.md` is the shared contract; `.codex/agents/` holds six TOML persona
files: lexi, dexter, gus, anna, titus, maisie. Each names one affinity —
lexi–wonder-lab, dexter–mass, gus–wonder-scholar, anna–wonder-prompt,
titus–wonder-build, maisie–wonder-studio. Lexi is federation lead for narrative
synthesis and final judgment. Dexter engineers, debugs, and simulates. Gus
researches and verifies. Anna architects prompts and workflows. Titus documents
and teaches. Maisie directs visual identity. `.codex/config.toml` sets
max_threads and max_depth. `images/agents/` holds one canonical black-tie
portrait per persona.

### T3 — machinery
Each `.codex/agents/<name>.toml` carries a `developer_instructions` block:
Identity, Role and affinity, Cognitive style, Operating method, Strengths and
growth edges, Collaboration, Output. `AGENTS.md` § Federation routing pairs each
agent to one affinity skill. The binding is bidirectional: each affinity's
`SKILL.md` carries a matching `## Reciprocal agent` section naming its agent
back. Each skill's `agents/openai.yaml` supplies a `default_prompt` invoking
`$skill-name`. `AGENTS.md` § Shared federation contract layers The Sieve and
Hyperplane Telemetry E/L/S/H across all six, and `.codex/config.toml` bounds
max_threads 6, max_depth 1.

### T4 — edges
`.codex/config.toml` caps the federation at max_threads 6 and max_depth 1 — no
agent spawns a sub-chain beyond one level. `AGENTS.md` holds agents are bounded
project specialists, not sovereign memory stores, and blocks irreversible action
under Sieve REVISE or HALT. README notes project-local custom-agent files are a
Codex-only feature; ChatGPT Work lacks them. Only six canonical black-tie
portraits may live under `images/`; `PUBLIC_EXPORT_MANIFEST.md` excludes every
`private-*` skill from this distribution. README also states this folder was
never Git-initialized or published before the mirror.

### T5 — frontier
README states the forward path directly: "A future plugin can package the stable
Lexideck skills for installation across projects and Work," resolving the present
boundary where project-local custom-agent files remain Codex-only while ChatGPT
Work gets only skills (`README.md:155`). Version `0.1.0` is "prepared as a public
release candidate," implying further releases beyond it (`README.md:159`).
`CONTRIBUTING.md` requires every pull request to confirm "the project still
discovers six custom agents and 19 public skills" before merge
(`CONTRIBUTING.md:22`). No other roadmap item names the federation specifically.

### Entity ledger

| entity | tier | locator | status |
|---|---|---|---|
| Codex (host/conductor) | T1 | `AGENTS.md:15`; `README.md:161` | referenced-external |
| `AGENTS.md` shared contract | T1 | `AGENTS.md` | present-verified |
| `lexi` / `dexter` / `gus` / `anna` / `titus` / `maisie` | T2 | `.codex/agents/<name>.toml:1` | present-verified |
| `.codex/config.toml` bounds | T2 | `.codex/config.toml:1-3` | present-verified |
| six canonical portraits | T2 | `images/agents/` | present-verified |
| `$the-sieve` ethics gate | T3 | `.agents/skills/the-sieve/SKILL.md:1-6`; `AGENTS.md:17` | present-verified |
| reciprocal-agent binding (bidirectional) | T3 | `.agents/skills/wonder-prompt/SKILL.md:11-13` | present-verified |
| Hyperplane Telemetry E/L/S/H | T3 | `AGENTS.md:18`; `.codex/agents/lexi.toml:24-25` | present-verified |
| "Codex skill validator" | T4 | `CONTRIBUTING.md:18` | claimed-in-prose-only |
| future cross-platform plugin | T5 | `README.md:155` | claimed-in-prose-only |

### Key facts

| claim | value | locator |
|---|---|---|
| custom agents | 6 | `.codex/agents/` |
| thread bound | `max_threads = 6` | `.codex/config.toml:2` |
| depth bound | `max_depth = 1` | `.codex/config.toml:3` |
| release version | `0.1.0` | `VERSION:1` |
| canonical portraits | 6 | `.gitignore:30-35` |

> `AGENTS.md:15` — "Codex is the host and conductor."
>
> `.agents/skills/wonder-prompt/SKILL.md:13` — "Anna is WonderPrompt's affinity."

**Cross-links:** B2 (the affinity skills' bodies) · B3 (the portrait allowlist) ·
B4 (the six TOMLs as manufactured output) · B5 (five affinity names descend from
the 2025 corpus).

---

## B2 — The nineteen-skill corpus

### T1 — essence
A skill is a reusable method Codex can load on demand: a markdown file pairing a
short frontmatter description with an instruction body, invoked by name or
triggered by matching intent. The nineteen-skill corpus is Lexideck 2026's public
method library, covering federation coordination, five WonderSuite-descended
creative and analytical engines, research and lookup, ethics review, persona
authoring, prompt craft, and portraiture. Skills hold technique, not personality;
six agents, defined elsewhere, apply them. Each of the nineteen ships paired with
a companion file so its method also runs inside a bare OpenAI-runtime context.

### T2 — structure
Nineteen directories sit under `.agents/skills/`, grouped by README into five
named bands: Federation and synthesis (orchestrate, great-magnet, the-sieve,
upsum); Core affinities, the five WonderSuite-descended engines plus mass;
Research and tools (search, deep-research, cartographer, computer-use); Prompt
and persona systems (prompt-engineering, hypershot-protocol, ptg-synthesis,
ptg-finishing); and Visual identity (portraits). Each directory holds exactly one
`SKILL.md` plus one `agents/openai.yaml`. One shared reference file,
`references/PTG-Corpus.md`, backs the two PTG skills only. Six personas each name
a primary affinity in prose; skills reciprocally name an agent, unenforced by
schema.

### T3 — machinery
Every `SKILL.md` opens with YAML frontmatter carrying only `name` and
`description`; the description is the router, front-loading "use when" triggers
and "not for" exclusions Codex matches against intent. The body is Markdown,
invoked as `$skill-name` (`AGENTS.md:54`), with no other frontmatter fields —
no tools, no license — anywhere. Every `agents/openai.yaml` is exactly four
lines: display_name, short_description, default_prompt echoing `$name` — a fixed,
unvarying companion shape. The wonder-* skills share a four-part method:
reciprocal agent, dimensional axes, phased protocol, primitive operations, plus
an explicit override clause.

### T4 — edges
No skill grants tools, memory, or execution; each assumes whatever Codex session
capabilities are already live and disclaims inventing bridges, APIs, or secrets
(`search/SKILL.md:16`; `deep-research/SKILL.md:91`). Recursion is capped:
deep-research names the default `agents.max_depth=1`, so a dispatched worker
cannot spawn further workers (`deep-research/SKILL.md:39`). the-sieve gates
irreversible action but is advisory prose, run inline by the acting agent, not
enforced by code. Public/private is a Git-ignore naming convention, not
filesystem security (`README.md:117`). ptg-finishing strips personal identifiers
before public deployment.

### T5 — frontier
`README.md:155` states the one forward claim this branch makes: "A future plugin
can package the stable Lexideck skills for installation across projects and Work"
— skills run project-local only today, not yet portable across ChatGPT surfaces.
`deep-research/SKILL.md:14` marks a present boundary meant to stay distinguished
from OpenAI's own hosted Deep Research feature, never merged into it.
`mass/SKILL.md:103` dates MASS_evolve's collaborative design to June 29, 2026 —
the corpus's most recent internal extension, evidence the simulation method is
still being added to, not closed.

### The roster

| skill | invocation | charter, compressed | status |
|---|---|---|---|
| cartographer | `$cartographer` | audits a documentation map against live source; small reversible corrections only | present-verified |
| computer-use | `$computer-use` | routes GUI tasks to the correct native desktop control surface | present-verified |
| deep-research | `$deep-research` | WonderScholar-first bounded multi-source investigation with evidence packets | present-verified |
| great-magnet | `$great-magnet` | bounded six-agent pass producing one facet per specialist on one target | present-verified |
| hypershot-protocol | `$hypershot-protocol` | meta-prompting with zero-contamination structural frames | present-verified |
| mass | `$mass` | Multi-Agent Semantic Simulator: builds runnable simulations, not descriptions | present-verified |
| orchestrate | `$orchestrate` | conducts the federation; dispatches bounded work and reconciles results | present-verified |
| portraits | `$portraits` | canonical public-register portraits from a fixed identity roster | present-verified |
| prompt-engineering | `$prompt-engineering` | structural clarity over "magic words" | present-verified |
| ptg-finishing | `$ptg-finishing` | calibrates a persona draft into a deployment-ready TOML | present-verified |
| ptg-synthesis | `$ptg-synthesis` | first-draft persona tensor from sparse inputs | present-verified |
| search | `$search` | grounds a focused question in current sources with direct citations | present-verified |
| the-sieve | `$the-sieve` | three-lens ethical gate: PASS / REVISE / HALT | present-verified |
| upsum | `$upsum` | compresses the live task into a continuity snapshot for handoff | present-verified |
| wonder-build | `$wonder-build` | knowledge construction: documentation, tutorials, learning paths | present-verified |
| wonder-lab | `$wonder-lab` | narrative generation, genre-agnostic | present-verified |
| wonder-prompt | `$wonder-prompt` | instruction design for system prompts and deployable frameworks | present-verified |
| wonder-scholar | `$wonder-scholar` | research method producing implementation-ready frameworks | present-verified |
| wonder-studio | `$wonder-studio` | art direction, concept through rendered image | present-verified |

### Key facts

| claim | value | locator |
|---|---|---|
| skill directories on disk | 19 | `.agents/skills/` |
| README's stated count | "19 portable, unprefixed Lexideck skills" | `README.md:115` |
| `AGENTS.md` stated count | "the 19 unprefixed project skills" | `AGENTS.md:46` |
| manifest's stated count | "Nineteen public or public-sanitized project skills" | `PUBLIC_EXPORT_MANIFEST.md:9` |
| companion file length | exactly 4 lines, all 19 | verified across every `agents/openai.yaml` |
| skills consuming PTG-Corpus | 2 | `ptg-synthesis/SKILL.md:75`; `ptg-finishing/SKILL.md:39-41` |

**Arithmetic check.** The tree holds 19 skill directories. README, `AGENTS.md`,
and `PUBLIC_EXPORT_MANIFEST.md` all say nineteen. **No discrepancy** — the count
is one of the few claims in this repository that is independently asserted three
times and verified against bytes.

> `.agents/skills/mass/SKILL.md:9` — "MASS builds things that run, not things that describe"

**Cross-links:** B1 (reciprocal agent bindings) · B4 (the two PTG skills and their
shared corpus) · B5 (five of these nineteen descend from the 2025 corpus).

---

## B3 — The publication boundary

### T1 — essence
The publication boundary decides what leaves Lexideck's private working node and
becomes the public Codex repository. It is a promotion rule, not a redaction
rule: files enter by explicit allowlist, never by copying the private tree
wholesale and deleting sensitive parts afterward. One naming convention carries
the weight — any path whose basename begins with `private-` is excluded, at any
depth, from what the public project can contain. Everything else the public
repository ships is presumed safe for anyone to read, by default, carrying no
private material at all.

### T2 — structure
Five documents carry the boundary: `PUBLIC_EXPORT_MANIFEST.md` states included
and deliberately excluded categories; `.gitignore` enforces most exclusions
mechanically at commit time; `CONTRIBUTING.md` binds contributors to the same
allowlist discipline; `USER.example.md` is the template for optional personal
context; `AGENTS.md` and README each restate the model in prose for the routing
agents. Two namespaces split public from private: unprefixed skills form the
nineteen-skill public register, while `private-<name>` and `local-<name>`
directories stay locally discoverable but Git-excluded. `.lexideck-local/` holds
the optional personal profile, ignored entirely.

### T3 — machinery
The stated rules and the shipped bytes agree everywhere this was directly tested.
`.gitignore`'s `private-*` pattern, unslashed, is a basename match that ignores a
directory at any depth — confirmed with `git check-ignore` against a synthetic
`.agents/skills/private-test/SKILL.md` path. The `images/agents/*`
block-then-unblock sequence correctly re-admits only the six named canonical
portraits after blanket-ignoring `images/*` first. `.lexideck-local/`,
`production_artifacts/`, `wiki/`, and `.env` ignore exactly as stated;
`.env.example` is correctly carved back out. The tracked tree contains zero
`private-*` paths and precisely six portraits.

### T4 — edges
`AGENTS.md` and README both state the convention's limit plainly: the `private-`
prefix is a routing and publication guard, not filesystem security, since a
process holding workspace access can still open an ignored file. Git's
ignore-matching stops a commit; it cannot stop a read. `CONTRIBUTING.md`
separately names a Codex skill validator and privacy-and-absolute-path scans as
required pre-pull-request checks, but no script, tool, or CI workflow
implementing either exists anywhere in the tracked tree — the described
enforcement is entirely a human review step, not code the repository runs.

### T5 — frontier
`CONTRIBUTING.md`'s unbuilt checks point forward: a Codex skill validator meant
to run against every changed skill package, and privacy-and-absolute-path scans
meant to run over the exact proposed release tree, both required before every
pull request — named present-tense obligations with no implementing file yet
checked into this tree. README's status section separately names a further, later
distribution surface: a future plugin that could package the stable Lexideck
skills for installation across projects and Work, extending today's allowlist
discipline toward an installable cross-project boundary someday, still unbuilt.

### The boundary, tested against the bytes

| rule as stated | locator | what the tree contains | holds? |
|---|---|---|---|
| files enter by explicit allowlist, never copy-then-delete | `PUBLIC_EXPORT_MANIFEST.md:26-28` | 60 tracked files, all matching the Included list | **holds** |
| any `private-`-prefixed basename excluded at any depth | `PUBLIC_EXPORT_MANIFEST.md:18`; `.gitignore:6` | `git check-ignore -v` on a synthetic path matches `.gitignore:6`; zero `private-*` tracked | **holds** |
| only six curated portraits permitted under `images/` | `README.md:149`; `.gitignore:25,27-35` | blanket-ignore then six explicit un-ignores; exactly six files tracked | **holds** |
| `.lexideck-local/` and `production_artifacts/` ignored | `.gitignore:2,16` | both match; neither exists in the tracked tree | **holds** |
| `.env`, `*.key`, `*.pem` ignored; `.env.example` kept | `.gitignore:38-42` | confirmed, including the `!` exception | **holds** |
| the prefix is a guard, not filesystem security | `README.md:117`; `AGENTS.md:48` | the repo's own text concedes it | **holds** (disclaims more than it promises) |
| a validator and privacy scans run before every PR | `CONTRIBUTING.md:18,25` | zero workflow files, zero validator files, anywhere | **unenforceable-by-construction** |

Six of seven rules hold against the bytes. The seventh is not a leak — it is an
obligation with no implementation, which is a different failure and worth naming
as one.

### Key facts

| claim | value | locator |
|---|---|---|
| tracked files | 60 | `git ls-files` at `a1bc8a6` |
| `.gitignore` lines | 48 | `.gitignore:1-48` |
| deliberately-excluded categories | 8 | `PUBLIC_EXPORT_MANIFEST.md:17-24` |
| commit author identity | `Lexideck Technologies <156171296+gusthemole@users.noreply.github.com>` | `git log` |

> `README.md:117` — "not filesystem security: a process with workspace access may still read ignored files"

**Cross-links:** B1 (the portrait allowlist is the persona asset set) · B2 (the
public register is the nineteen skills) · B5 (the commit author identity is the
receipt that both corpora share one author).

---

## B4 — The PTG persona-authoring pipeline

### T1 — essence
PTG stands for Persona Tensor Generator (`ptg-synthesis/SKILL.md:3`). It is a
two-stage manufacturing pipeline: ptg-synthesis drafts a rough-in persona tensor
from sparse inputs — name, role, goals, optional emoji seed — and ptg-finishing
calibrates that rough draft into a deployment-ready Codex custom-agent
definition. Both skills draw shared trait vocabulary, methodology, and structural
examples from one file, `references/PTG-Corpus.md`, loaded only when needed. The
six `.codex/agents/*.toml` files are this pipeline's shipped output: personas
manufactured, not hand-authored.

### T2 — structure
`PTG-Corpus.md` organizes five named parts: psychographic trait vocabulary across
seven dimensions — cognitive style, social, emotional framework, emotional
intelligence, qualitative intelligence, technical capabilities, interest/cultural
(`:13-57`); synthesis methodology's three phases, Signal Acquisition and Vector
Expansion, Dimensional Mapping, System Manifestation (`:59-77`); a worked
competency-decomposition example (`:79-88`); the FEV apparatus of three
injections, three regulation modalities Alpha/Beta/Gamma, and a three-step
transformation pipeline (`:90-108`); and a twelve-item complete-section checklist
(`:110-126`).

### T3 — machinery
Checked against ptg-finishing's own structure and deployment-form specs
(`SKILL.md:14,45-54`), all six shipped TOMLs conform on `name`, `description`,
and a `developer_instructions` block opening `# Agent Name`, and every one
carries Identity, Role and affinity, Cognitive style, Operating method, Strengths
and growth edges, Collaboration, and Output. FEV coupling, also named in that
same structure list, appears in only `lexi.toml:24`, one of six. Competency
tensor, required by ptg-synthesis's output frame (`SKILL.md:37`), plus the
numeric scalars ptg-finishing's checks presuppose, appear in zero of six.

### T4 — edges
Both skills load `PTG-Corpus.md` only when needed, retrieving "the smallest
relevant section" (`ptg-synthesis/SKILL.md:75`) and never pattern-matching a
persona to the corpus example, whose numeric values teach "grammar only"
(`PTG-Corpus.md:88`). ptg-synthesis must not deploy a rough-in without the
finishing pass (`SKILL.md:79`). ptg-finishing must not invent identity, only
calibrate existing evidence (`SKILL.md:8`), and its public-persona check strips
names, schedules, budgets, health details, and private-memory claims before reuse
(`SKILL.md:25`). `PTG-Corpus.md:127` permits omitting a section only when it
adds no operational behavior.

### T5 — frontier
The only stated forward path is external: "the private Node may pair public
defaults with private counterparts such as `$private-portraits` or
`$private-ptg-synthesis`, but those implementations do not belong here"
(`README.md:119`) — a companion synthesis skill this public repo names but
explicitly does not contain. `AGENTS.md:40` marks `references/PTG-Corpus.md` a
"shared PTG reference," implying continued reuse rather than retirement. No file
proposes new trait dimensions, extra regulation modalities beyond Alpha/Beta/
Gamma, a seventh persona, or a successor corpus.

### The conformance gap

Ten specified fields are present in all six shipped personas. Two are not.

| field the method specifies | locator | present in | verdict |
|---|---|---|---|
| `name`, `description`, `developer_instructions` block | `ptg-finishing/SKILL.md:47-52` | 6/6 | conforms |
| Identity · Role and affinity · Cognitive style · Operating method · Strengths and growth edges · Collaboration · Output | `ptg-finishing/SKILL.md:14` | 6/6 each | conforms |
| **FEV coupling** | `ptg-finishing/SKILL.md:14` | **1/6** (only `lexi.toml:24`) | partial |
| **Competency tensor** | `ptg-synthesis/SKILL.md:37-41` | **0/6** | absent |
| **Numeric trait scalars** (any `0.xx`) | `ptg-finishing/SKILL.md:15,31-37` | **0/6** | absent |

**Why this is structural, not sloppy.** The gap is not a checklist executed
badly. It is that ptg-finishing's own Structure check (`:14`) *silently drops*
"Competency tensor" relative to what ptg-synthesis's output frame (`:37`) and
`PTG-Corpus.md`'s complete-section checklist (`:116`) both require. The finishing
stage does not check for the thing the synthesis stage is told to produce — and
ptg-finishing's Scalar-calibration section (`:31-37`) presumes scalars exist to
calibrate, when none are present in any shipped persona. One stage of a two-stage
pipeline is calibrating an input that never arrives.

### Key facts

| claim | value | locator |
|---|---|---|
| PTG expansion | Persona Tensor Generator | `ptg-synthesis/SKILL.md:3` |
| corpus content sections | 5 | `PTG-Corpus.md:5-11` |
| trait vocabulary dimensions | 7 | `PTG-Corpus.md:13-57` |
| synthesis phases | 3 | `PTG-Corpus.md:59-77` |
| FEV regulation modalities | 3 (Alpha, Beta, Gamma) | `PTG-Corpus.md:98-102` |
| ptg-finishing ordered checks | 6 | `ptg-finishing/SKILL.md:10-19` |
| complete-section checklist items | 12 | `PTG-Corpus.md:110-126` |
| TOMLs carrying FEV coupling | 1 | `lexi.toml:24` |
| TOMLs carrying a competency tensor or any scalar | 0 | all six |

> `references/PTG-Corpus.md:127` — "Omit a section only when it would add no predictive"

**Note on FEV.** The acronym recurs across `AGENTS.md`, `PTG-Corpus.md`, and the
persona files, and is **never expanded anywhere in the tracked tree**. Grepped
exhaustively. It is used as though defined; it is not.

**Cross-links:** B1 (the six TOMLs as routed personas) · B2 (the two PTG skills
in the roster) · B3 (the public-persona check is the boundary's per-artifact arm).

---

## B5 — Descent from WonderSuite

This branch is the answer to a question the tree poses and does not answer: five
of the nineteen skills carry the names of a 2025 corpus by the same author. Is
that inheritance or coincidence?

**Verdict: direct textual descent, with one layer amputated.**

All five matched pairs carry their WonderSuite namesake's core taxonomy — axis
names, primitive-operation signatures, parameter-space vocabularies — into
Lexideck's `SKILL.md` files essentially verbatim, while surrounding procedural
prose is compressed and rewritten. The two corpora share one author: WonderSuite's
files self-brand as a product of Lexideck Technologies as far back as March 2025,
and Lexideck 2026's squashed commit is authored by
`Lexideck Technologies <156171296+gusthemole@users.noreply.github.com>` — the same
account that owns the WonderSuite repository. This is not two strangers
converging on the same words.

### The descent table

| WonderSuite artifact | Lexideck artifact | relation | deciding evidence |
|---|---|---|---|
| `WonderBuild.txt:10` | `wonder-build/SKILL.md:24` | verbatim carry-over | all six axis labels identical, e.g. "Linear to Networked" |
| `WonderLab.txt:156` | `wonder-lab/SKILL.md:56` | verbatim carry-over | primitive signature identical: `DescribeRealm(realm, features, atmosphere)` |
| `WonderPrompt.txt:10` | `wonder-prompt/SKILL.md:22` | verbatim carry-over | all five axes and spectrum pairs identical, e.g. "Explicit to Implicit" |
| `WonderScholar.txt:118` | `wonder-scholar/SKILL.md:86-89` | verbatim carry-over + new material grafted on | Innovation Mapping's four labels identical: "Orthodox, Progressive, Boundary-Pushing, or Revolutionary" |
| `WonderStudio.txt:21` | `wonder-studio/SKILL.md:24` | verbatim carry-over | style-space entries verbatim, e.g. "Anime Meets Medieval Churrasco" |

### What was amputated

The drop is uniform across all five and is the most informative fact in this
branch. Gone entirely:

- **The Open Variable Protocol** — a JS-pseudocode meta-prompt layer with
  Variable Structure Patterns, numeric adaptive-context variables
  (`expertise_level` 0–1), composition and hierarchical-expansion mechanisms, and
  worked `context =>` arrow-function examples (`WonderBuild.txt:116-287` and
  parallels). Only the primitive *names and parameter tuples* survived, flattened
  into prose lists.
- **The bang-command API** — `!info`, `!help {topic}`, `!tutorial start {topic}`,
  `!list commands and features`, present identically in all five `.txt` files.
- **Structured single-line invocation** — e.g.
  `!WonderBuild domain="{DOMAIN}" user="{USER_PROFILE}"` (`WonderBuild.txt:89`).
- **The CSV `Category,ID,Name,Description` schema** — lookup IDs and per-entry
  glosses (`WonderLab.txt:21`, `WonderStudio.txt:20`). Lexideck kept bare names
  as inline comma lists.
- **`WonderSuite.txt` itself** — the 67 KB composite pitched for 200k+-token
  context models. Lexideck has no composite equivalent.

The pattern: **the executable-looking layer was removed and the taxonomy was
kept.** A prompt corpus that had begun growing a pseudo-API shed it on the way to
becoming a skill corpus.

### Born in Lexideck

| with no WonderSuite ancestor | locator | apparent source |
|---|---|---|
| "Charitable Interpretation Research Method (Widening the Blanket)" | `wonder-scholar/SKILL.md:15-28` | near-duplicate prose also in `gus.toml:22-23`; neither file dates itself |
| "Bounded Research Frame" (`$deep-research` integration) | `wonder-scholar/SKILL.md:130-155` | tied to a Lexideck-only workflow |
| "Anti-contamination note" | `wonder-prompt/SKILL.md:127-129` | tied to `hypershot-protocol`, no WonderSuite ancestor |
| "Framework modularity (override clause)" in all five | `wonder-build/SKILL.md:110-112` | no WonderSuite equivalent; the sources have no override mechanism |
| 13 further skills | `.agents/skills/<name>/SKILL.md` | repo-wide grep for "wonder" finds nothing outside the five plus one cross-reference |
| the six personas as *characters* | `.codex/agents/*.toml` | WonderSuite's engines are explicitly persona-free |

### Timeline

| date | event | locator |
|---|---|---|
| 2025-03-01 | WonderSuite initial upload: five engines, composite, README, LICENSE | `321b04d` |
| 2025-03-14 | "2.0": bang-command layer, Open Variable sections, Lexideck branding | `9e2f377`; `CHANGELOG.md:7,13` |
| 2025-04-25 | logo assets replaced/added | `7778059`, `85f59a5` |
| 2026-01-07 | README revised for WonderSuite 2.0 | `092037f` |
| 2026-07-16 | Lexideck 2026 squash-committed as one commit, `VERSION 0.1.0` | `a1bc8a6` |

**The dating limit, stated plainly.** WonderSuite's twelve commits give a real
build order. Lexideck's single squashed commit destroys its own entirely. The
transfer can be dated only as "at or before 2026-07-16" — over a year after
WonderSuite reached its committed 2.0 state. Which of the five was adapted first,
whether they moved together or across a long span, and how many drafts preceded
the committed state are all unrecoverable from these bytes.

**Cross-links:** B2 (five of the nineteen are the descendants) · B3 (the shared
commit-author identity) · the companion study at
[`OpenCnid/axes-of-wonder`](https://github.com/OpenCnid/axes-of-wonder), which
maps the ancestor on its own terms.

---

## Cross-section: general → current → future

Reading the trellis across rather than down.

| | **general (T1)** | **current (T2–T3)** | **frontier (T4–T5)** |
|---|---|---|---|
| **B1 federation** | six named specialists under one contract | six TOMLs, bidirectional affinity binding, `max_depth=1` | a plugin that would package skills across surfaces — unbuilt |
| **B2 skills** | a method library loaded on demand | 19 dirs, two-field frontmatter, four-line companion | portability past project-local — unbuilt |
| **B3 boundary** | allowlist promotion, not redaction | `.gitignore` enforces; six of seven rules verified | a validator and privacy scans — named, unbuilt |
| **B4 PTG** | personas manufactured, not hand-authored | corpus → synthesis → finishing → six TOMLs | a private counterpart skill, explicitly not here |
| **B5 lineage** | an earlier corpus by the same author | taxonomy carried, pseudo-API amputated | — (a completed transition, not a plan) |

**The shape that falls out.** Every branch's frontier column says *unbuilt*, and
says so in the repository's own words. This is a corpus at version `0.1.0` that
is unusually explicit about the difference between what it ships and what it
intends — the manifest, the contributing guide, and the README all name
obligations no file implements. Read as a defect that is a finding; read as
honesty it is a virtue. The map records it as neither, only that it is the case
in seven distinct places.

---

## Provenance

- **Subject pin:** commit `a1bc8a6b608f2cf4b98716c22dc75ffab3205987`, dated
  2026-07-16, `VERSION 0.1.0`.
- **Verified:** 2026-07-22.
- **Locator convention:** `path:line` against the tree at the pinned commit.
  Section locators (`file` § heading) where a line number would be unstable.
- **Method:** the chain-of-density system mode —
  [OpenCnid/chain-of-density](https://github.com/OpenCnid/chain-of-density).
  Fixed 90-word tier budget, all five tiers shipped, own words throughout,
  quotes under fifteen words and attributed.
- **How the branches were built.** Five read-only sub-agents, one per branch,
  each working from an identical verbatim ground block and returning against a
  rigid frame (five tiers at a held budget, an entity ledger with locators, a
  key-facts table, verbatim anchors, cross-link candidates, and a mandatory
  "uncovered" slot). Siblings could not see one another. The trunk, the
  cross-section, and the cross-link lattice were composed afterward, by hand,
  from what the branches returned — no sibling adjudicated another's findings.
- **What the method cannot do here.** A single squashed commit means this
  repository cannot be reverse-engineered from its build order the way a
  multi-commit project can. Every "when" question about Lexideck 2026 is
  answered, at best, with its one date. The companion study of the ancestor
  corpus has twelve commits and correspondingly better answers.
- **A human and an AI built this map together.** Disclosed because the house rule
  is to disclose it.
