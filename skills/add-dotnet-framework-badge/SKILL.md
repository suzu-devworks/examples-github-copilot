---
name: add-dotnet-framework-badge
description: "Add or update a README .NET Framework badge using shields.io dynamic XML by reading LatestFramework from src/Directory.Build.props. Use when asked to add a .NET badge, framework badge, or shields dynamic XML badge."
---

# Add .NET Framework Badge

## Purpose

Add a README badge that shows the framework value from `src/Directory.Build.props` (`LatestFramework`) via shields.io dynamic XML.

## Use When

- The user asks to add a .NET badge to README.
- The badge value should come from `LatestFramework` in `src/Directory.Build.props`.
- The user wants a dynamic badge managed by shields.io.

## Inputs

- Repository owner (for example: `suzu-devworks`)
- Repository name (for example: `examples-dotnet-metaprogramming`)
- Target branch for raw file URL (default: `main`)

## Required Badge Settings

- `logo=dotnet`
- `label=Framework`
- `color=%23512bd4`
- Query must extract `LatestFramework` using XPath: `//LatestFramework`

## Markdown Template

```md
[![Framework](https://img.shields.io/badge/dynamic/xml?url=https%3A%2F%2Fraw.githubusercontent.com%2F{OWNER}%2F{REPO}%2Fmain%2Fsrc%2FDirectory.Build.props&query=%2F%2FLatestFramework&logo=dotnet&label=Framework&color=%23512bd4)](https://github.com/{OWNER}/{REPO})
```

Replace:

- `{OWNER}` with repository owner
- `{REPO}` with repository name

## Placement

Insert the badge directly below the README title (`# ...`) and above the first section heading.

## Validation Checklist

1. README contains exactly one new badge line in the top section.
2. Badge URL uses `dynamic/xml` and points to `src/Directory.Build.props` on raw.githubusercontent.com.
3. Query is `//LatestFramework` (URL-encoded as `%2F%2FLatestFramework`).
4. Badge parameters include `logo=dotnet`, `label=Framework`, and `color=%23512bd4`.
5. Existing README content order remains unchanged.
