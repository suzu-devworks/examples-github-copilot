# README Structure

Choose sections based on the repository rather than following a fixed template.

Every section should help readers understand this repository.

Do not include advice about how documentation should be organized unless it is itself a characteristic of this repository.

## Required sections

- What is this repository?
- What topics are covered?

## Conditional sections

- What should I prepare before development?

---

## What is this repository?

### Condition

Always include this section.

### Purpose

Explain the repository's role within the `examples` collection.

This section should be largely consistent across repositories.

### Include

- The purpose of the repository.
- How it relates to the `examples` collection.
- The overall approach or philosophy.

### Avoid

- Project-specific details.
- Lists of technologies.
- Setup instructions.

---

## What topics are covered?

### Condition

Always include this section.

### Purpose

List the main topics covered by the repository so readers can quickly understand its scope.

### Include

- Use a bullet list.
- Include 3-10 concise items.
- Focus on the repository's primary themes.
- Primary technologies and frameworks.
- High-level concepts.
- Main subject areas, when relevant.

### Avoid

- A complete list of projects.
- Detailed feature lists.
- Implementation details.

---

## What should I prepare before development?

### Condition

Include this section only when one or more of the following apply:

- Multiple Dev Container definitions are provided.
- Additional preparation is required before opening the Dev Container (for example, certificates or local resources).
- Development uses multiple Docker Compose files or Docker Compose starts additional services that readers should know about.
- Development or CI requires running repository-provided setup scripts to prepare the local environment or required resources.

Otherwise, omit this section entirely.

### Purpose

Describe repository-wide prerequisites or preparation that readers should know before starting development.

### Include

- Which Dev Container to use and when, if multiple are provided.
- Additional preparation required before opening the Dev Container.
- Repository-wide Docker Compose services and why they are used.
- Repository-wide development environment customizations that affect development.
- Repository-wide assets that must be prepared before development or CI.
- Instructions for running any repository-provided setup scripts, including example command lines in a code block.

### Avoid

- Standard Dev Container usage.
- Build or run instructions.
- Project-specific setup.
- Repository structure.
- Configuration details that are self-explanatory.
- Information that readers can easily infer from the repository.
- Restating configuration files without explaining why readers should care.
