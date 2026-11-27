# AGENTS

## Purpose

- To maintain a collection of custom files for GitHub Copilot that can be used across other repositories.
- To preserve existing implementations as a record of learning.
- To implement improvements if better approaches are discovered.

## Project Structure

- Files here are not placed in folders directly referenced by GitHub Copilot, such as `/.github` or `/.agents`.
- While files may be placed in `/.github` or `/.agents` for testing purposes, they must not be included in repository commits.

## Architecture

- Although the primary target is GitHub Copilot, priority is given to content and configurations that are compatible
  with other AI agents whenever possible.

## Design Principles

- Source code, comments, and documentation must all be written in English.
- Adhere to existing conventions.
- Prioritize simple implementations.
- Prioritize the use of modern language features if they improve readability or maintainability.

## Workflow

- Keep diffs minimal to ensure they are reviewable.
- For complex, ambiguous, or high-impact tasks, align on the approach before making significant changes.
- Do not add or update dependencies without prior confirmation.
- Always seek confirmation before making breaking changes.
- Verify changes after editing.

## Boundaries

- Do not create pull requests or perform operations on remote repositories unless instructed to do so.
- Keep exploratory temporary files outside Git-managed paths and remove them after work is complete.
- Do not leave temporary or generated files in the repository unless they are intended as project artifacts.
