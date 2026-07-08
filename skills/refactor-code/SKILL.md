---
name: refactor-code
description: Refactor source files without changing behavior
confidence: 1.0
learned_from: "manual:refactor-runner"
learned_at: "2026-07-08T00:00:00.000Z"
usage_count: 0
success_count: 0
failure_count: 0
negative_examples: []
---

# Refactor Code

## Instructions

1. Read source files one at a time.
2. Skip tests, fixtures, generated output, dependencies, `.git`, `.gitagent`, and `memory`.
3. Preserve public exports, callback compatibility, thrown errors, return shapes, and observable behavior.
4. Prefer small behavior-preserving improvements:
   - Replace callback-style async code with async/await when compatibility can be preserved.
   - Add validation to public-facing functions.
   - Extract repeated magic strings and numbers into named constants.
   - Remove unused imports and obviously unreachable code.
   - Add JSDoc comments to exported functions.
5. After each file, report the file path and a short summary of what changed.

## Output Format

For each changed file:

- **File**: path
- **Changes**: concise behavior-preserving summary
- **Validation**: mention preserved behavior or tests/checks run
