---
name: migration
description: Use only when the user explicitly asks for a framework, API, dependency, or version migration
confidence: 1.0
learned_from: "manual:agent-structure"
learned_at: "2026-07-08T00:00:00.000Z"
usage_count: 0
success_count: 0
failure_count: 0
negative_examples: []
---

# Migration

## Instructions

1. Identify the source version, target version, and compatibility constraints before editing.
2. Read official migration notes or local upgrade documentation when available.
3. Make small commits or file groups that preserve behavior at each step.
4. Update imports, configuration, tests, and documentation that are required by the migration.
5. Record risky assumptions and any follow-up checks in memory.
6. If the user asked for normal refactoring rather than migration, stop using this skill and use `refactor-code` instead.

## Output Format

- **Scope**: what changed
- **Compatibility**: behavior or API guarantees preserved
- **Validation**: checks run or required
- **Follow-ups**: remaining migration risks
