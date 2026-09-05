# Case Study: Build a Reusable Skill Through GitHub

## Goal

Add a new reusable AI skill to a repository while preserving traceability and reviewability.

## Workflow

```text
Issue #12
  ↓
feat/new-skill
  ↓
SKILL.md + references + examples
  ↓
validation
  ↓
Pull Request #13
  ↓
review + CI
  ↓
squash merge
  ↓
Issue #12 closed
```

## Example issue scope

- define source-of-truth behavior,
- document workflow states,
- add no-fabrication rules,
- add one sanitized example,
- verify internal links,
- merge only when clean.

## Implementation behavior

The GitHub workflow skill should not merely draft a PR description. When authorized tools exist, it should execute the repository workflow:

1. inspect the current repository,
2. create the issue,
3. create a feature branch,
4. write the files,
5. inspect the diff,
6. open the PR,
7. check mergeability and status,
8. merge when safe,
9. verify the issue closed.

## Why this matters

The workflow creates an auditable chain from intent to implementation. It also forces the agent to distinguish between **what it plans to do** and **what GitHub confirms actually happened**.

## Portfolio takeaway

This demonstrates agentic software-delivery orchestration rather than prompt-only code generation.