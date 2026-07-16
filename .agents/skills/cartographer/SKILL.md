---
name: cartographer
description: Audit and maintain a project documentation map against current source files, repositories, and authoritative external facts. Use when documentation may be stale, a catalogue or index needs checking, project status claims need live verification, or a documentation tree needs honest tiering. A clean pass is successful; apply only small reversible factual corrections unless broader structural edits are explicitly authorized.
---

# The Cartographer

Keep the map faithful to the territory. Re-survey existing documentation; do not manufacture updates merely to make the pass look productive.

## Resolve the scope

- Use the page, directory, project, tier, or repository named by the user.
- If nothing is named, locate the project's documentation index or catalogue and use it as the reading key.
- If no index exists, inventory the documentation tree and state the inferred scope before continuing.

## Audit method

1. Read the current documentation before testing its claims.
2. Identify claims about status, versions, dates, repositories, dependencies, or implemented features.
3. Re-ground unstable claims against live authoritative evidence.
4. Check for structural drift: undocumented additions, retired components still marked active, misplaced maturity tiers, broken links, or duplicated guidance.
5. Separate factual corrections from structural proposals.

## Repository verification

For every repository claim in scope:

1. Read the live repository through an authorized connector or direct repository access, not a cached search result.
2. Record the latest relevant commit's short SHA, author date, and message when status or activity is being checked.
3. Compare the evidence with the documentation.
4. If the repository is private or unavailable, report that limitation and do not guess.
5. Never call a project dormant, inactive, current, or complete without current evidence.

## Editing policy

- Apply small, reversible factual corrections when the request authorizes maintenance.
- Propose new pages, splits, removals, or major retiering before applying them unless the user explicitly authorized structural edits.
- Delete nothing by default. Move retired material into an available superseded or archive location.
- Preserve dense, load-bearing documentation. Longer without more information is inflation.

## Report

Return the scope, evidence checked, corrections made, structural proposals, inaccessible sources, and a clear clean-pass statement when nothing changed. Include commit evidence for repository-status checks.

## Constraints

- Prefer primary sources.
- Do not expose private user information or local machine paths in public documentation.
- Pass consequential edits through `$the-sieve`.
- Use `$orchestrate` only when a specialist or inaccessible tool boundary genuinely requires it.
