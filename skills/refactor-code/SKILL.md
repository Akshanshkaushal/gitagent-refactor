---
name: refactor-code
description: Refactor source files without changing behavior
confidence: 1.0
learned_from: "manual:refactor-runner"
learned_at: "2026-07-08T13:34:26.719Z"
usage_count: 2
success_count: 2
failure_count: 0
negative_examples: []
last_session_id: "2e31ca7c-ba28-46a4-8ba5-d175eb3f08a1"
last_changed_files: ["src/math-utils.js","src/user-service.js"]
last_learning_summary: "Successful behavior-preserving refactor across 2 source file(s): src/math-utils.js, src/user-service.js. Keep future runs scoped to source files and avoid committing runtime memory artifacts."
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
