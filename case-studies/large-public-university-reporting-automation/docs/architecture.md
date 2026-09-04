# Solution Architecture

## Design objective

Reduce recurring manual report-processing effort without removing the human review, exception handling, follow-up, or accountability required by the reporting process.

## Architecture pattern

```text
Current source data
        │
        ▼
Purpose-built Excel / Power Query processing layer
        │
        ├── repeatable transformations
        ├── recurring preparation logic
        ├── consistent processing rules
        └── structured reporting output
        │
        ▼
Reviewable output
        │
        ▼
Human review
        │
        ├── exception interpretation
        ├── follow-up
        ├── management action
        └── accountability
```

The implementation used multiple purpose-built Excel and Power Query files aligned to recurring biweekly and monthly reporting deliverables rather than a single monolithic application.

## Separation of concerns

The architecture deliberately separated two kinds of work:

**Deterministic processing** — transformations and preparation steps that could be expressed as repeatable rules.

**Human judgment** — determining whether information was appropriate, interpreting exceptions, deciding what follow-up was necessary, and acting on the results.

This boundary was more important than the choice of tool. The objective was not maximum automation; it was appropriate automation.

## Processing model

The original workflow repeatedly required people to manipulate source information before it became reviewable. The redesigned workflow encoded those recurring operations into reusable query logic.

At a high level:

```text
Before:
Source → manual preparation → manual transformation → reconciliation → review → action

After:
Source → deterministic processing layer → reviewable output → human review → action
```

## Why the architecture remained lightweight

The problem did not require a custom application, machine-learning model, or new enterprise platform. The repeatable portion of the process followed deterministic rules and could be addressed inside tools appropriate to the existing reporting environment.

That reduced implementation complexity while preserving the existing responsibility and review model.

## Public-package limitation

This architecture is intentionally generalized. Original query logic, workbook structures, source-system details, field names, source files, report layouts, and institutional identifiers are not included in the public package.