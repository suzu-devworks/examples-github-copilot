---
name: repository-instructions-refine
description: Optimize repository-specific instructions while preserving rules that prevent real AI mistakes.
---

# Repository Instructions Refinement

Review the existing repository-specific instruction file.

## Goal

Reduce instruction size while preserving practical value for AI coding agents.

The final result should contain only rules that help prevent real repository-specific mistakes.

## Evaluation Criteria

For each instruction determine:

* Is it still necessary?
* Is it already obvious from the repository?
* Is it already enforced by tooling?
* Is it duplicated by another instruction?
* Is it obsolete?
* Is it too generic to provide meaningful value?

## Classification

Classify each instruction as:

### Keep

The instruction remains valuable.

### Simplify

The instruction is useful but can be shorter or clearer.

### Remove

The instruction is redundant, obsolete, generic, or obvious.

## Analysis Output

For each instruction provide:

### Instruction

{current instruction}

### Classification

Keep | Simplify | Remove

### Reason

Explain the decision.

## Final Output

Start the output with YAML front matter that includes:

* description
* applyTo

Produce a section named:

## Optimized Instructions

Return a revised instruction set that:

* Removes redundancy
* Removes generic advice
* Removes obsolete rules
* Removes rules already enforced by tooling
* Preserves repository-specific constraints
* Preserves rules that prevent recurring AI mistakes

Prefer a final instruction file under 20 lines.

When in doubt, remove general guidance and keep only repository-specific constraints.
