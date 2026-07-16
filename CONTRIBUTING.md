# Contributing to Lexideck 2026 Codex Public

Thank you for helping improve Lexideck. Keep contributions portable, reviewable, and safe to publish.

## Contribution boundary

- Work from the Public project and promote files by explicit allowlist. Never create a release by copying a private node and deleting sensitive material afterward.
- Keep public skills unprefixed and usable without personal memory, private continuity, private corpora, or machine-specific absolute paths.
- Do not add any file or directory whose basename begins with `private-`.
- Do not add secrets, credentials, personal profiles, private wiki material, generated working history, or noncanonical images.
- Keep generated output under ignored working directories such as `production_artifacts/`.

## Skill changes

- Match each skill directory name to the `name` in `SKILL.md`.
- Keep triggering scope and exclusions in the frontmatter `description`.
- Keep `agents/openai.yaml` aligned with `SKILL.md`, including a `default_prompt` that invokes `$skill-name`.
- Run the Codex skill validator against every changed skill package.

## Before a pull request

- Confirm the project still discovers six custom agents and 19 public skills.
- Validate TOML and skill metadata.
- Verify every README image link and the six-portrait allowlist.
- Run privacy and absolute-path scans over the exact proposed release tree.
- Inspect the Git allowlist before staging, and explain what changed and how it was tested.

By contributing, you agree that your contribution is licensed under the repository's GNU General Public License v3.0 (`GPL-3.0-only`).
