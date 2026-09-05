---
name: basketball-business-operations
description: Run repeatable basketball-business workflows across leads, athlete onboarding, evaluations, packages, sessions, payments, team operations, and retention without mixing policies or inventing live data.
metadata:
  version: "0.1.0"
  example: true
---

# Basketball Business Operations

Use this skill for basketball training or club operations that need clear state, source-of-truth discipline, and repeatable execution.

## First rule: identify the operating context

A request may concern:

- private/small-group development,
- team/club operations,
- camps/clinics,
- another explicitly named program.

Do not mix prices, contracts, schedules, payment states, athlete records, or policies across contexts.

## Source hierarchy

Use, in order:

1. current user instruction,
2. current live business system,
3. current-season contracts/forms/trackers,
4. current operating references,
5. historical examples.

Historical material is evidence of past practice, not current policy.

## State models

### Training lead

```text
New → Contacted → Qualified → Assessment Scheduled → Assessed → Offer Sent → Active Client
                                                  ↘ Not Now / Closed
```

### Active client

```text
Onboarded → Scheduled → Training → Progress Review → Renewed
                                      ↘ Paused / Completed
```

### Team player

```text
Registered → Tryout Scheduled → Evaluated → Decision → Accepted → Onboarded → Active Season → Closeout
```

## Lead workflow

Capture:

- athlete name or internal ID,
- parent/guardian contact if applicable,
- age/grade,
- goals,
- experience,
- preferred training format,
- availability,
- source of inquiry,
- current status,
- next action/date.

Do not quote a price unless it is retrieved from the current approved offer source.

## Athlete assessment workflow

Separate:

- identity/background,
- observed skills,
- strengths,
- development priorities,
- recommended focus,
- next reassessment point.

A useful development structure is:

```text
assessment → 2 primary priorities + 1 maintenance priority → training block → reassessment
```

Do not convert subjective observations into fake precision.

## Session operations

Before the session:

- confirm athlete/client,
- confirm package/payment eligibility if required,
- confirm time/location,
- load current development priorities.

After the session:

- record attendance,
- record actual work completed,
- record one or two observations,
- record next adjustment,
- update remaining package/session state if the source system supports it.

## Team/club operations

Typical workflow:

```text
registration → evaluation → roster decision → contract/fees → uniform → practices → tournaments → season evaluation
```

For roster or payment questions, retrieve the relevant live tracker first.

## Financial and payment controls

Never infer that a payment was made because:

- a player is active,
- a contract exists,
- a payment date passed,
- a receipt template exists.

Use the current payment record.

## Privacy rule

Public documentation should contain only fictional or aggregated examples. Keep real contact details, medical information, payment records, signatures, evaluations, and athlete identifiers in private systems.

## Example request

> Review all active leads and tell me which ones need follow-up this week.

Expected behavior: read the live lead system, classify each record by state and next-action date, return only actionable follow-ups, and never invent missing status or pricing.
