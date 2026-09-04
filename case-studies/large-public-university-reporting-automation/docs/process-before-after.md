# Process Before and After

## Before

The recurring reporting portfolio required repeated preparation and review work across multiple biweekly and monthly deliverables.

```text
Source data
    ↓
Manual preparation
    ↓
Manual transformation
    ↓
Reconciliation
    ↓
Human review
    ↓
Follow-up / management action
```

Five administrative staff participated in the process. When the combined preparation-and-review workload was normalized to a biweekly operating cycle, it exceeded 50 staff-hours on average.

A significant portion of the effort occurred before people reached the work that actually required judgment.

## Redesigned process

```text
Current source data
    ↓
Reusable Power Query processing
    ↓
Reviewable reporting output
    ↓
Human review / exception handling
    ↓
Follow-up / management action
```

The redesigned process moved recurring transformation and preparation rules into reusable Power Query logic. Once current source data was available, the automated processing for applicable deliverables ran in minutes.

## What changed

The redesign changed **how information became reviewable**. It did not remove the reporting requirement or transfer accountability to software.

People continued to determine whether information was appropriate and current, interpret exceptions, perform follow-up, and decide what action was necessary.

## Capacity Recovery interpretation

The original 50+ staff-hour figure represents combined recurring preparation-and-review workload. The redesign reduced repeatable processing substantially, but the figure should not be interpreted as 50+ hours of guaranteed labor savings per cycle. Human review and other necessary activities remained.

The defensible outcome is **capacity recovery from repetitive processing**, not elimination of the entire original workload.