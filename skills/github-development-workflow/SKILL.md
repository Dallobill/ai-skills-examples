---
name: github-development-workflow
description: Execute a disciplined GitHub Issue → Branch → Implementation → Validation → Pull Request → Review → Merge workflow without fabricating repository state.
metadata:
  version: "0.1.0"
  example: true
---

# GitHub Development Workflow

Use this skill when work should be executed through GitHub rather than described abstractly.

## Canonical workflow

```text
Issue
  ↓
Feature branch
  ↓
Implementation
  ↓
Validation
  ↓
Commits
  ↓
Pull request
  ↓
Review / CI
  ↓
Fixes if needed
  ↓
Merge
  ↓
Issue closeout
```

## Rules

1. Inspect the repository before modifying it.
2. Use an issue to define scope when the work is substantial enough to benefit from traceability.
3. Branch from the correct base branch.
4. Keep changes aligned to issue scope.
5. Validate before opening or merging the PR.
6. Read actual PR/CI state; never claim `mergeable`, `passing`, or `merged` from assumption.
7. Do not bypass failed checks unless the user explicitly accepts the risk and repository policy allows it.
8. Close the issue through the PR when possible.

## Issue template

A useful issue contains:

- objective,
- current problem,
- scope,
- acceptance criteria,
- out-of-scope items,
- validation requirements.

## Branch naming

Prefer readable names such as:

- `feat/add-session-tracking`
- `fix/payment-status-sync`
- `docs/skill-examples`
- `refactor/job-retry-state`

## Pull request standard

A PR should explain:

- what changed,
- why,
- validation performed,
- known limitations,
- issue linkage.

## Review standard

Before merge, verify:

- diff matches requested scope,
- no secrets or private data were added,
- generated artifacts are intentional,
- tests/checks are acceptable,
- documentation matches behavior,
- PR is mergeable.

## Example request

> Add a new reusable skill to this repository and merge it if validation is clean.

Expected behavior: create an issue, create a feature branch, implement the skill, inspect the changed files, open a PR linked to the issue, inspect mergeability/CI, and merge only when the repository state supports it.
