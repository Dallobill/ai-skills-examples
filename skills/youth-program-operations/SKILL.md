---
name: youth-program-operations
description: Convert a live youth-program curriculum, calendar, group rotation, and delivery log into weekly staff-ready operations while preserving sequence, safety, and evidence.
metadata:
  version: "0.1.0"
  example: true
---

# Youth Program Operations

Use this skill when an agent must turn a structured youth-program system into executable weekly plans rather than inventing activities from scratch.

## Operating principle

The live program system is the source of truth. Plans are not evidence of delivery.

## Required sources

Read only what is needed for the request:

1. program calendar,
2. group/facility rotation,
3. lesson index or curriculum library,
4. staff-sheet template,
5. delivery log when actual completion matters,
6. assessment/coverage records when reporting outcomes.

## Weekly planning workflow

### 1. Resolve the real week

Identify:

- program week,
- unit/block,
- closures or shortened days,
- lesson sequence,
- scheduled groups,
- session lengths,
- facility mode.

Never assume a session occurred because it was scheduled.

### 2. Reconcile surviving visits

For each group, order the actual available visits by date/time.

Default pattern:

- first curriculum visit → Lesson A,
- second curriculum visit → Lesson B,
- later visits → reinforcement, approved alternative, makeup, or assessment.

If a shortened week leaves only one meaningful visit during a sport sequence, prioritize the next undelivered sport lesson when the program rules explicitly permit it.

### 3. Retrieve exact lesson content

Preserve:

- lesson ID,
- objective,
- activity names,
- equipment,
- timing,
- teaching cues,
- safety rules,
- age-band adaptation,
- shared-space adaptation.

Do not replace a defined lesson with a generic activity unless the source system allows a backup.

### 4. Build staff-ready materials

Each session sheet should contain:

- date/time,
- group,
- age band,
- lesson ID/title,
- objective,
- equipment,
- setup,
- timed lesson segments,
- coaching cues,
- safety limits,
- space modification,
- post-session outcome fields.

### 5. Separate planned from delivered

After staff runs the session, record actual evidence separately:

- actual date,
- group,
- lesson ID,
- result,
- actual minutes,
- attendance if collected,
- observed outcome,
- next adjustment.

A planned session does not count as delivered coverage.

## Coverage rules

- Count a unique `Group + Core Lesson ID` once.
- Repeats may count as visits but not duplicate core completion.
- `Not Run` adds no coverage.
- Alternatives do not replace another core lesson unless the program was explicitly redesigned.

## Safety and adaptation

Keep the learning goal stable. Modify:

- distance,
- equipment,
- space,
- pressure,
- rules,
- support level.

Prefer participation and control over waiting, elimination, or excessive competition.

## Example request

> Build next week's staff packet for all five groups and adjust for a Wednesday closure.

Expected behavior: read the live calendar and rotation, reassign surviving visits, preserve lesson sequence, generate group-specific sheets, and leave the delivery log untouched until sessions actually occur.
