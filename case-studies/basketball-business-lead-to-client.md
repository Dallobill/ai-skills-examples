# Case Study: Basketball Lead → Active Client

## Problem

A basketball development business receives inquiries through social media, referrals, forms, and word of mouth. Without a defined workflow, leads become scattered messages and follow-up depends on memory.

## Fictional source snapshot

A lead record contains:

- Athlete: Jordan Example
- Grade: 8
- Goal: improve ball handling and finishing
- Experience: school team
- Preferred format: small group
- Availability: weekday evenings
- Lead source: referral
- Current state: Qualified
- Next action: assessment scheduling

No live price is stored in this example.

## Skill behavior

The `basketball-business-operations` skill should:

1. identify this as a private-development lead rather than a team/club player,
2. read the current lead record,
3. preserve the state as `Qualified`,
4. identify `Assessment Scheduled` as the next state,
5. avoid quoting a package price because no current offer source was provided,
6. generate the next operational action rather than a generic marketing response.

## State progression

```text
New
 ↓
Contacted
 ↓
Qualified
 ↓
Assessment Scheduled
 ↓
Assessed
 ↓
Offer Sent
 ↓
Active Client
```

At the assessment stage, the system may create two primary development priorities and one maintenance priority, then carry those into the training block.

## Example post-assessment record

```text
Primary priority 1: handle under pressure
Primary priority 2: finishing off two feet
Maintenance priority: catch-and-shoot footwork
Reassessment: after training block
```

These are fictional examples. A production system should store real observations in a private source, not a public repository.

## Why this matters

The system distinguishes **workflow state** from conversational history. An agent can answer:

- Which leads need follow-up?
- Who has been assessed but has no offer?
- Which active clients are due for reassessment?
- Who has no next action scheduled?

without guessing from old messages.

## Portfolio takeaway

This pattern demonstrates lightweight CRM design, state machines, source-of-truth discipline, and human-in-the-loop service operations.