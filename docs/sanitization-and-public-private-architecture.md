# Sanitization & Public/Private Architecture

This repository is a public portfolio. It is intentionally separated from production operating repositories and live connected systems.

## Public layer

Safe to publish:

- generic workflow logic,
- fictional examples,
- reusable state machines,
- architecture patterns,
- validation rules,
- placeholder schemas,
- sanitized case studies.

## Private layer

Keep private:

- real client/player names,
- phone numbers and email addresses,
- dates of birth,
- medical information,
- signatures,
- individual payment records,
- internal source-system URLs/IDs,
- real contracts and unpublished pricing,
- private evaluation notes,
- internal schedules or staffing details,
- credentials/secrets/tokens.

## Sanitization checklist

Before moving anything from a production system into this repository:

1. remove real names and identifiers,
2. replace organizations with generic descriptions when needed,
3. remove source URLs and file IDs,
4. replace real prices with placeholders or clearly fictional values,
5. remove real dates/schedules unless they are fully genericized,
6. remove private policy text that is not intended for publication,
7. remove person-level evaluations and payment data,
8. verify examples cannot be reverse-mapped to a real participant,
9. inspect the final Git diff before merge.

## Recommended architecture

```text
PRIVATE
production skill repo
live Drive / CRM / database / code repositories
real policies + data
        ↓
   sanitized abstraction
        ↓
PUBLIC
ai-skills-examples
fictional examples + reusable patterns
```

The public repo demonstrates **system design and agent workflow engineering**. It is not a backup of production data.

## Design principle

A good public example should reveal the reasoning structure without revealing the operating secrets or personal data that made the production system specific.