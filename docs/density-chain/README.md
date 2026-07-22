# `docs/density-chain/` — how to consume this map

> Instructions for agents and humans reading the study. The repo
> [README](../../README.md) is the friendlier front door.

**Note for agents:** the root `AGENTS.md` in this repository is **upstream's**,
and it governs the *corpus*, not this study. It is unmodified and should be read
as Lexideck Technologies' instructions to their own federation. This file governs
only the two artifacts under `docs/`.

## What's in here

| file | what it is |
|---|---|
| [`DENSITY-CHAIN.md`](DENSITY-CHAIN.md) | ground truth. A trunk plus five branches, each a fixed-length five-tier chain. |
| [`DENSITY-CHAIN.html`](DENSITY-CHAIN.html) | the same content, rendered as a clickable lattice. **Markdown wins** on any disagreement. |
| [`../SPARK-STEERING.md`](../SPARK-STEERING.md) | the capability-axis diagnosis: which axis this corpus occupies, which is short. |

## Reading it efficiently

- **Pick your tier by budget, not by ambition.** All five tiers of a branch are
  the same length. Loading T1 costs what T5 costs; the difference is density, not
  size. Skim with T1, work with T3, argue with T5.
- **The traverse is fixed.** T1 general essence → T2–T3 machinery actually in the
  tree → T4–T5 edges and stated frontier. A deeper tier only *adds*; it never
  corrects a shallower one. If it did, that's a defect — file it.
- **Read the branch you need, not the trunk plus everything.** Branches are
  independent by construction. The trunk exists to tell you which one you want.
- **Status labels are load-bearing.** `present-verified` means a file backs the
  claim. `claimed-in-prose-only` means the README says it and no file does.
  `referenced-external` means it lives outside the repo. Treat them as different
  kinds of fact, because they are.

## The rules that bind anyone updating this

1. **Upstream wins.** When the map and the corpus disagree, the corpus is right
   and the map gets fixed. One direction, no exceptions.
2. **No claim without a locator.** Every statement carries `path:line` into the
   tree at the pinned commit. A number you remember is a number you don't write.
3. **Fixed tier budget.** Ninety words. Rewrite at the same length; never append.
   The budget is the whole engine — without it, "add detail" produces a longer
   summary rather than a denser one.
4. **All five tiers ship.** The densest tier is not the best tier; readers pick.
5. **Don't edit upstream files.** Our additions live in `docs/`, `assets/`, and
   `index.json`. If a fix belongs in the corpus, it belongs
   [upstream](https://github.com/Lexideck-Technologies/Lexideck2026), not here.
6. **Humor stays in the READMEs.** Tiers, ledgers, key facts, and provenance are
   bone-dry. Jokes in ground truth age like milk.

## Re-verifying

`index.json` carries `pinned_commit` and `verified_against_source`. To check
whether this map has gone stale:

```bash
git ls-remote https://github.com/Lexideck-Technologies/Lexideck2026.git HEAD
```

If that SHA differs from `pinned_commit`, the map describes an older tree. A
stale pin is a flag for a human or agent session to re-verify at the source — it
is never grounds for editing the map to match a guess.

## Method

The chain-of-density method, system mode:
[OpenCnid/chain-of-density](https://github.com/OpenCnid/chain-of-density). The
methodology lives there and is linked, never copied — one canonical home, no
drift.
