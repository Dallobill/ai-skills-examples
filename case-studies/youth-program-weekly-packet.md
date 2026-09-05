# Case Study: Weekly Youth Program Operations Packet

## Problem

A youth program runs multiple groups through a shared gym using a structured curriculum. Staff need one weekly packet that tells them exactly what to run, while the program director needs delivery evidence kept separate from planning.

A one-off chatbot answer is not enough because the plan depends on:

- the current curriculum week,
- closures,
- group rotations,
- session length,
- age band,
- facility sharing,
- prior delivery state.

## Fictional source snapshot

Assume the live system says:

- Week 4 is a movement + passing week.
- Lesson A = `M04-A — Reaction Gates`.
- Lesson B = `P01 — Ready, Pass, Receive`.
- Wednesday is closed.
- Five groups have different visit counts.
- Some sessions use a shared half-court.
- Friday contains 30-, 40-, and 60-minute blocks.

## Skill behavior

The `youth-program-operations` skill:

1. resolves the actual week and closure,
2. orders each group's surviving visits,
3. assigns first visit = A, second visit = B, later visits = reinforcement,
4. retrieves the exact lesson content,
5. adapts timing to 30/40/60 minutes,
6. applies age-band and shared-gym modifications,
7. produces one staff sheet per actual session,
8. leaves the delivery log untouched until sessions occur.

## Example output structure

```text
Weekly Packet
├── Week overview
├── Master Lesson A
├── Master Lesson B
├── Group 1 session sheets
├── Group 2 session sheets
├── Group 3 session sheets
├── Group 4 session sheets
└── Group 5 session sheets
```

Each staff sheet contains:

- date/time,
- group and age band,
- lesson ID,
- objective,
- equipment,
- timed segments,
- coaching cues,
- safety boundaries,
- facility modification,
- post-session outcome fields.

## Why this matters

The workflow converts an AI interaction into a controlled operating system:

```text
source data → weekly decision logic → staff artifact → actual delivery → evidence log → next week
```

The critical design choice is that **planned work and completed work remain separate states**. That prevents reports from treating a schedule as evidence of implementation.

## Portfolio takeaway

This pattern generalizes beyond athletics. Any recurring field operation with schedules, standard procedures, staff handoffs, and completion evidence can use the same architecture.