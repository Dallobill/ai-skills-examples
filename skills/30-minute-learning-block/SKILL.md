---
name: 30-minute-learning-block
description: Run a focused 30-minute learning session using retrieval, explanation, guided practice, active recall, and a precise next starting point.
metadata:
  version: "0.1.0"
  example: true
---

# 30-Minute Learning Block

Use this skill for compact, repeatable study sessions where continuity and retention matter more than covering large amounts of material.

## Default structure

```text
0-5 min   Retrieval
5-20 min  New concept
20-27 min Guided practice
27-30 min Recall + next step
```

## 1. Retrieval

Start from the learner's most recent stopping point.

Ask for or reconstruct:

- what concept was last studied,
- what the learner remembers without notes,
- what was confusing,
- what should be reviewed before adding new material.

Do not restart from the beginning unless needed.

## 2. New concept

Teach one tightly scoped concept.

Prefer:

- plain language first,
- a visual or concrete example,
- one worked example,
- one contrast showing what changes when a condition changes.

Avoid introducing several abstractions at once.

## 3. Guided practice

Give the learner a small problem and let them reason before supplying the polished answer.

Use progressive difficulty:

```text
recognize → explain → apply → transfer
```

## 4. Recall closeout

End with a no-notes check:

- What did we learn?
- Why does it work?
- What would change in a similar problem?

Record:

- Completed
- Understood
- Needs review
- Next starting point

## Continuity rule

The next session should resume from the exact unresolved concept, not from a generic curriculum sequence.

## Example request

> Give me today's 30-minute lesson on nested loops. Yesterday I understood how the inner index advances but I was confused about why some pairs never appear.

Expected behavior: retrieve that exact confusion, visualize the pair-generation pattern, teach the boundary rule, give one short practice problem, and save the next starting point.
