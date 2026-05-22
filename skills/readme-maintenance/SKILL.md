---
name: readme-maintenance
description: 'Create or update repository root and project-level README.md files. Use when documenting repositories, refreshing setup steps, standardizing README structure, or drafting concise English README content across ecosystems.'
argument-hint: 'What README files should be created or updated?'
license: MIT
user-invocable: true
---

# README Maintenance

Create or update README.md files in concise English.

## Scope

- Repository root README.md: the README.md file at repository root.
- Project README.md: a README.md in a directory with a project manifest (for
  example, .csproj, package.json, pyproject.toml).
- Project detection notes: if multiple manifests exist in one directory, treat
  it as a solution/workspace candidate and ask which target to update. For
  nested manifests, use the closest manifest directory unless a broader scope is
  explicitly requested.
- Out of scope: non-README markdown files unless explicitly requested.

## Rule Routing

- Read policy first: [policy rules](./references/policy.md).
- For repository root README, use [repository root rules](./references/repository-root-readme-guidelines.md).
- For project README, use [project rules](./references/project-readme-guidelines.md)
  and matching language rules under `references/<language>/`.
- In this repository, project README rules are .NET:
  [dotnet project rules](./references/dotnet/dotnet-readme-guidelines.md).

## Normative Levels

- `MUST`: required behavior.
- `SHOULD`: recommended behavior; allow exceptions with user direction.

## Quick Workflow

1. `MUST`: identify target README files and classify each as repository root
  or project.
2. `MUST`: route to the correct rules (policy, scope-specific,
  language-specific).
3. `MUST`: create and update a task list before editing when the work is
  multi-step.
4. `MUST`: review existing README content, or create from the matching
  template.
5. `MUST`: confirm the scope in one short line before editing (target,
  purpose, badge change yes/no).
6. `MUST`: show a patch preview summary and get user approval before applying
  edits.
7. `MUST`: update missing or inconsistent content while preserving accurate
  sections.
8. `MUST`: run final checks in the matching scope guideline.

## Decision Gates

- `MUST`: confirm before changing badges, license wording, CI snippets, or
  sample commands/code when not explicitly requested.
- `MUST`: for root README updates, preserve existing badges unless badge
  changes are explicitly requested.

## Constraints

- `SHOULD`: prefer non-destructive proposal flow for substantial changes
  (patch review, branch, or PR) unless the user asks for direct in-place edits.
- `MUST`: record evidence for each major edit (which files were referenced and
  why).
- `MUST`: use auto-fix only for formatting-safe issues; apply manual edits if
  wording or meaning might change.
- `MUST`: for edge cases (submodules, generated folders, vendored content,
  secrets), avoid adding or rewriting related sections without explicit
  direction.

## Validation

- `MUST`: run markdownlint for each changed README and fix reported issues.

## Draft Short-Term Guardrails

Use these guardrails by default for repository root and project README updates.

- `MUST`: run a pre-edit scope check with `target`, `goal`, and
  `badges changed: yes/no`.
- `MUST`: provide a pre-apply diff review that summarizes section-level
  changes before applying a patch.
- `MUST`: keep root badges unchanged unless explicit user approval is provided.
- `MUST`: include an evidence log listing source files used to justify edits.
- `SHOULD`: use a non-destructive proposal path for larger updates (patch-first,
  branch, or PR) instead of silent direct rewrites.

Recommended validation command:

```bash
npx -y markdownlint-cli <path-to-readme>
```

## References

- Policy rules: [policy rules](./references/policy.md)
- Repository root rules:
  [repository root rules](./references/repository-root-readme-guidelines.md)
- Project rules: [project rules](./references/project-readme-guidelines.md)
