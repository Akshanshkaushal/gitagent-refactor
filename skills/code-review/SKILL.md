---
name: code-review
description: Review code for correctness, maintainability, security, and behavior regressions
confidence: 1.0
learned_from: "manual:agent-structure"
learned_at: "2026-07-08T00:00:00.000Z"
usage_count: 0
success_count: 0
failure_count: 0
negative_examples: []
---

# Code Review

## Instructions

1. Read the requested files or pull request diff before judging behavior.
2. Prioritize findings that could cause bugs, regressions, security issues, data loss, or broken user workflows.
3. Keep style-only comments secondary unless they hide a real maintainability risk.
4. Reference exact files and line numbers when reporting issues.
5. Do not rewrite unrelated code while reviewing.

## Output Format

For each issue:

- **File**: path
- **Line**: number
- **Severity**: critical / warning / info
- **Description**: what can go wrong
- **Fix**: suggested change
