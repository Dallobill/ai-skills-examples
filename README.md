# AI Skills Examples

A public, sanitized portfolio of reusable AI operating skills.

This repository demonstrates how I structure AI-assisted workflows as repeatable systems instead of one-off prompts. The examples are adapted from real operating patterns across program management, basketball operations, software development, GitHub workflows, and daily learning.

> **Privacy note:** This is a showcase repository. Names, organizations, source-system URLs, real schedules, prices, client/player records, internal policies, and other private operational details have been removed or replaced with fictional examples.

## What this demonstrates

- source-of-truth-first agent design
- reusable `SKILL.md` operating procedures
- workflow state machines
- separation of planning vs. completed work
- human-in-the-loop operational controls
- connected-tool execution patterns
- validation and no-fabrication rules
- privacy-aware public/private repository architecture
- Issue → Branch → PR → Review → Merge delivery

## Example skills

| Skill | Purpose |
| --- | --- |
| [Youth Program Operations](skills/youth-program-operations/SKILL.md) | Turn a curriculum, schedule, staff rotation, and delivery log into weekly staff-ready operations. |
| [Basketball Business Operations](skills/basketball-business-operations/SKILL.md) | Manage leads, athletes, evaluations, packages, scheduling, payments, and retention without mixing business contexts. |
| [Coding Development](skills/coding-development/SKILL.md) | Make code changes from repository context with minimal, validated implementation. |
| [GitHub Development Workflow](skills/github-development-workflow/SKILL.md) | Execute disciplined Issue → Branch → PR development workflows. |
| [30-Minute Learning Block](skills/30-minute-learning-block/SKILL.md) | Run compact learning sessions using retrieval, explanation, practice, and recall. |

## Case studies

- [Weekly Youth Program Operations Packet](case-studies/youth-program-weekly-packet.md)
- [Basketball Lead → Active Client](case-studies/basketball-business-lead-to-client.md)
- [Issue → Merge Skill Build](case-studies/issue-to-merge-skill-build.md)

## Fictional source examples

The case studies are backed by deliberately fictional source snapshots so reviewers can see the full source → skill → execution model without exposing production information.

- [Youth Program Source Snapshot](examples/fictional-youth-program/source-snapshot.md)
- [Basketball Business Source Snapshot](examples/fictional-basketball-business/source-snapshot.md)

## Repository structure

```text
ai-skills-examples/
├── README.md
├── skills/
│   ├── youth-program-operations/
│   ├── basketball-business-operations/
│   ├── coding-development/
│   ├── github-development-workflow/
│   └── 30-minute-learning-block/
├── case-studies/
├── examples/
└── docs/
```

## Design model

```text
Live source / repository / connected system
                ↓
             AI skill
                ↓
       operating rules + state
                ↓
        action / artifact / update
                ↓
             validation
                ↓
         next system state
```

A skill is not just a prompt. It defines **how the agent should work**: what sources to read, what rules to preserve, what it may update, what it must never invent, and how to verify completion.

## Public vs. private architecture

Production skills and live operating data belong in private systems. This public repository contains only sanitized patterns, generic procedures, and fictional examples suitable for portfolio review.

See [Sanitization & Public/Private Architecture](docs/sanitization-and-public-private-architecture.md).

## Why this repository exists

The goal is to demonstrate a practical approach to AI workflow engineering: use models for reasoning, skills for repeatable procedure, connected systems for current state, and validation to prevent the agent from confusing intent with completed work.

## Status

This repository is example-driven and will expand as additional production workflows are generalized into safe public patterns.