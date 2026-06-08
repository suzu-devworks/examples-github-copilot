---
name: repository-instructions-discover
description: Discover repository-specific rules that are difficult for AI coding agents to infer automatically.
---

# Repository Instructions Discovery

Analyze this repository and identify repository-specific rules that an AI coding agent is unlikely to infer reliably.

## Goal

Extract only high-value repository-specific instructions.

The result should help AI coding agents avoid mistakes while keeping instruction files short and maintainable.

## Exclude

Do NOT include:

* Programming language best practices
* Framework best practices
* Coding style preferences
* Linting rules
* Formatting rules
* Generic software engineering advice
* Information that is obvious from the repository structure
* Information already enforced by tooling

Examples to exclude:

* Use TypeScript strict mode
* Avoid any
* Follow SOLID principles
* Write maintainable code
* Use ESLint
* Use Prettier

## Focus Areas

Look for:

* Architecture constraints
* Layering rules
* Dependency direction rules
* Folder-specific restrictions
* Generated code restrictions
* Legacy code restrictions
* Deployment/runtime constraints
* Domain-specific business rules
* Repository-specific testing requirements
* Common mistakes an AI coding agent is likely to make

## Candidate Rules

For each proposed rule provide:

### Rule

* {rule}

### Why

Explain why the rule exists.

### Prevents

Explain what AI mistake the rule prevents.

### Confidence

Choose one:

* High
* Medium
* Low

## Final Output

Start the output with YAML front matter that includes:

* description
* applyTo

Produce a section named:

## Recommended Instructions

Include only rules that are:

* High confidence
* Repository-specific
* Useful for preventing real AI mistakes

Keep the final instruction set under 20 lines.

Prefer concise rules such as:

* Do not edit generated files.
* Avoid changes under legacy/.
* Database access only through repositories.
* New API endpoints must be implemented under src/api/v2.

Favor constraints and restrictions over documentation.
