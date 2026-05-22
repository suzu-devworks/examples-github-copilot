# examples-github-agents

## What is the purpose of this repository?

This repository provides reusable skills and references for maintaining and improving GitHub Copilot agent workflows,
with a current focus on practical README maintenance standards.

It might be useful for developers who have the same problem.

However, please note that the code discussed here is based on my personal opinion and may contain many inaccuracies.

I do not accept responsibility for any issues caused by using content from this repository.

## Technology Stack

- GitHub Copilot Agent Skills: Skill definitions, references, and templates
- Markdown: Skill and policy documentation
- Node.js tooling: Markdown lint validation via markdownlint-cli

## Setup

### DevContainer

Open this repository in a VS Code Dev Container to use the preconfigured environment.

### Build-Pre Environment Setup

Install Node.js and npm if they are not already available in your environment.

### Test Environment Setup

No additional test-only dependencies are required.

### Build and Test

```bash
npx -y markdownlint-cli README.md
npx -y markdownlint-cli "skills/**/*.md"
```
