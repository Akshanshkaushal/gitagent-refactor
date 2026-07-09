---
name: refactor-code
description: Use for plain source-code refactoring requests; improve code quality without changing behavior
confidence: 1.0
learned_from: "manual:refactor-runner"
learned_at: "2026-07-08T13:48:35.271Z"
usage_count: 3
success_count: 3
failure_count: 0
negative_examples: []
last_session_id: "7949a2a9-f733-45e3-a517-d1f6c4518447"
last_changed_files: ["src/math-utils.js","src/user-service.js"]
last_learning_summary: "Successful behavior-preserving refactor across 2 source file(s): src/math-utils.js, src/user-service.js. Keep future runs scoped to source files and avoid committing runtime memory artifacts."
---

# Refactor Code

## Instructions

1. Read source files one at a time.
2. Skip tests, fixtures, generated output, dependencies, `.git`, `.gitagent`, and `memory`.
3. Preserve public exports, function signatures, callback compatibility, thrown errors, return shapes, and observable behavior.
4. Prefer small behavior-preserving improvements:
   - Replace callback-style internals with async/await only when callback compatibility and public signatures are preserved.
   - Add validation to public-facing functions.
   - Extract repeated magic strings and numbers into named constants.
   - Remove unused imports and obviously unreachable code.
   - Add JSDoc comments to exported functions.
5. After each file, report the file path and a short summary of what changed.
6. Before writing a file, compare the proposed code against the original public API. If an exported function loses a parameter, changes sync/async behavior, removes callbacks, or changes return shape, do not write that change.
7. Prefer small scoped edits over rewriting an entire file when that reduces tool-call size and risk.
8. When the user asks for a pull request, use normal non-destructive git commands to create a new branch, commit only the target source changes, push the branch, and open a PR.

## Output Format

For each changed file:

- **File**: path
- **Changes**: concise behavior-preserving summary
- **Validation**: mention preserved behavior or tests/checks run
