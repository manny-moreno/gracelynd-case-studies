# Technology Decisions

## Selected technologies

- Microsoft Excel
- Power Query

## Why Power Query

The recurring processing layer was deterministic: the same categories of preparation and transformation work had to be performed repeatedly as new source data became available.

Power Query provided a practical way to encode that transformation logic into reusable steps rather than rebuilding the processing manually during every reporting cycle.

## Why Excel remained part of the solution

The objective was operational improvement, not technology replacement for its own sake. Excel was appropriate to the reporting context and provided a familiar environment for reviewable outputs while Power Query handled repeatable transformation logic.

## Technologies deliberately not required

The solution did not require:

- a custom software application;
- an AI or machine-learning model;
- a new enterprise reporting platform; or
- a large systems implementation.

Those technologies can be valuable when the problem requires them. Here, they would have added complexity without addressing a capability gap in the repeatable portion of the workflow.

## Decision principle

Tool selection followed the nature of the work:

```text
Repeatable + rule-based processing
             ↓
Deterministic automation
             ↓
Excel + Power Query
```

The lesson is not that Power Query is universally the correct tool. It is that automation architecture should be proportionate to the operational problem.

## Public-package limitation

Specific workbook designs, query expressions, field mappings, source-system schemas, report names, and organization-specific business rules are intentionally excluded because they are unnecessary to demonstrate the architectural decision and could expose internal operational information.