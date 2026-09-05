---
name: coding-development
description: Make repository-grounded code changes with minimal scope, explicit assumptions, validation, and regression awareness.
metadata:
  version: "0.1.0"
  example: true
---

# Coding Development

Use this skill for implementation, debugging, refactoring, and technical design work inside an existing codebase.

## Core rule

Read the codebase before proposing changes. Existing architecture and conventions are stronger evidence than generic best practices.

## Implementation workflow

### 1. Resolve the request

Identify:

- requested behavior,
- affected user flow,
- likely files/modules,
- acceptance criteria,
- constraints,
- whether the request changes data contracts or public interfaces.

### 2. Inspect before editing

Read:

- relevant source files,
- nearby tests,
- package/build configuration,
- project conventions,
- related interfaces/types,
- migrations when data models are involved.

Separate confirmed facts from assumptions.

### 3. Choose the smallest complete change

Prefer:

- extending existing abstractions,
- preserving naming and module boundaries,
- reusing current helpers,
- avoiding unrelated cleanup.

Do not redesign the system unless the task requires it.

### 4. Implement

Keep the change coherent. If behavior changes, update the associated test or add a focused regression test when practical.

### 5. Validate

Run the relevant subset of:

- tests,
- typecheck,
- build,
- lint,
- formatter,
- migration validation,
- manual reproduction.

Report what actually ran. Do not claim a command passed if it was not executed.

## Debugging workflow

```text
reproduce → isolate symptom → identify layer → form hypotheses → gather evidence → fix root cause → regression test
```

Avoid changing multiple unrelated layers at once unless the evidence requires it.

## Architecture workflow

When asked to design rather than implement, evaluate:

1. requirements,
2. constraints,
3. system boundaries,
4. data ownership,
5. contracts/interfaces,
6. failure modes,
7. observability,
8. security/privacy,
9. tradeoffs,
10. migration path.

## Example request

> Add a retry state to failed background jobs without changing the API response shape.

Expected behavior: inspect the current job model and worker flow, identify the smallest compatible change, add or update tests, run targeted validation, and summarize exact files changed and remaining risks.
