# Reporting Automation at a Large Public University

**Capacity Recovery case study | Microsoft Excel + Power Query**

> **50+ staff-hours → minutes of repeatable processing**

A recurring administrative reporting portfolio at a large public university required five staff members to prepare and review multiple biweekly and monthly reporting deliverables. The combined workload exceeded 50 staff-hours on average when normalized to a biweekly operating cycle.

The redesign separated repeatable data processing from work requiring human judgment. Microsoft Excel and Power Query were used to encode recurring transformation logic into reusable processing layers. Once current source data was available, the automated processing ran in minutes and produced outputs ready for human review, exception handling, follow-up, and management action.

## Why this repository package exists

This package documents the solution as **sanitized technical proof-of-work**. It focuses on the problem-solving approach, architecture, technology decisions, controls, and human/automation boundary without publishing source data, internal workbooks, organization-specific identifiers, credentials, or proprietary operational details.

## Outcome

- More than **50 staff-hours on average per biweekly operating cycle** were associated with preparation and review across the original recurring reporting portfolio.
- Five administrative staff participated in the process.
- The reporting supported 33 departments, more than 60 managers, and a workforce of more than 2,000 employees.
- Multiple Power Query-based files automated repeatable processing across applicable recurring deliverables.
- Once current source data was available, the automated processing layers ran in **minutes**.
- Human review and accountability remained part of the process.

The 50+ staff-hour figure describes the scale of the original combined preparation-and-review workload. It is not a claim that every original staff-hour was eliminated or converted directly into labor-cost savings.

## Capacity Recovery

The project illustrates Gracelynd's operating method:

**Discover → Measure → Separate → Automate → Recover**

1. **Discover** where recurring operational effort is being consumed.
2. **Measure** the workload and establish a defensible baseline.
3. **Separate** repeatable processing from work requiring human judgment.
4. **Automate** the repeatable layer with technology appropriate to the problem.
5. **Recover** human capacity for higher-value work while preserving accountability.

> Technology handles repeatability. People handle judgment. The organization recovers capacity.

## Technical documentation

- [`docs/architecture.md`](docs/architecture.md) — solution architecture and processing model.
- [`docs/process-before-after.md`](docs/process-before-after.md) — how the operating workflow changed.
- [`docs/human-automation-boundary.md`](docs/human-automation-boundary.md) — what was automated and what remained human-controlled.
- [`docs/technology-decisions.md`](docs/technology-decisions.md) — why Excel and Power Query were appropriate.
- [`docs/controls-and-lessons.md`](docs/controls-and-lessons.md) — controls, limitations, and lessons from the implementation.

## Canonical case study

The business-facing case study is published on Gracelynd & Company:

https://gracelynd.com/work/large-public-university-reporting-automation/

## Disclosure

This solution was developed by Gracelynd's founder while serving in an administrative role at a large public university. The university was not a Gracelynd client. No endorsement by the university is stated or implied.

This public package intentionally excludes original source data, internal reports, workbook files, screenshots, employee information, organization-specific system details, and identifying institutional information. Descriptions and diagrams are generalized to demonstrate the solution pattern without exposing protected operational material.