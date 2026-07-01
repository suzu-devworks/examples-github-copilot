---
name: markdown-quality
description: Keep Markdown files consistently formatted and lint-free after editing.
---

# Markdown Quality

Apply this workflow whenever you create or modify Markdown files.

## General

Prefer repository-defined scripts or tasks when they are readily available.

Do not spend time searching for alternative formatting or linting commands.

## Formatting

If the repository provides a Markdown formatter, run it after editing.

Prefer existing repository scripts or tasks over invoking formatter commands directly.

Do not introduce unrelated formatting changes.

## Linting

Only run `markdownlint-cli2` when the repository root contains either:

- `.markdownlint-cli2.yaml`
- `.markdownlint-cli2.jsonc`

Prefer an existing repository script or task that invokes `markdownlint-cli2`.

Otherwise, use:

```bash
npx -y markdownlint-cli2 "**/*.md"
```

If supported, automatically fix issues:

```bash
npx markdownlint-cli2 --fix "**/*.md"
```

Run the linter again until no automatically fixable issues remain.

Do not use `markdownlint-cli`.

## Preserve Meaning

Formatting and linting must not change the meaning of the document.

Avoid unnecessary modifications to:

- front matter
- headings
- tables
- links
- code blocks
- reference definitions

## Final Check

Before completing the task:

1. Ensure formatting is consistent.
2. Ensure Markdown lint passes.
3. Review automatic formatting changes.
4. Report any remaining issues that require manual intervention.
