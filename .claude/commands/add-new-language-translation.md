---
name: add-new-language-translation
description: Workflow command scaffold for add-new-language-translation in everything-claude-code.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /add-new-language-translation

Use this workflow when working on **add-new-language-translation** in `everything-claude-code`.

## Goal

Adds a new language translation for documentation, including agents, commands, rules, examples, and core docs.

## Common Files

- `docs/<lang>/README.md`
- `docs/<lang>/CONTRIBUTING.md`
- `docs/<lang>/TERMINOLOGY.md`
- `docs/<lang>/agents/*.md`
- `docs/<lang>/commands/*.md`
- `docs/<lang>/rules/**/*.md`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Create new language directory under docs/ (e.g., docs/pt-BR/ or docs/zh-CN/).
- Add translated versions of core docs (README.md, CONTRIBUTING.md, TERMINOLOGY.md, etc.).
- Add translated agents documentation (docs/<lang>/agents/*.md).
- Add translated commands documentation (docs/<lang>/commands/*.md).
- Add translated rules documentation (docs/<lang>/rules/**/*.md).

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.