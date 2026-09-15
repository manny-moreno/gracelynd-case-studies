# Human–Automation Boundary

## Principle

The system separates **judgment** from **repeatability**.

> **Technology handles repeatability. People handle judgment. The organization recovers capacity.**

Automation does not decide what Gracelynd should say publicly. It executes an already-governed decision reliably.

## Human responsibilities

Humans retain authority for deciding publication suitability, reviewing claims and confidentiality, approving disclosures and visuals, approving channel copy, authorizing channels, granting final publication approval, and deliberately selecting production execution.

These are control points, not inefficiencies to remove.

## Automation responsibilities

Automation retrieves metadata, parses structured state, evaluates explicit rules, checks prior publication state, retrieves approved copy, prepares payloads, invokes an authorized external transaction, captures results, builds and writes updated metadata, re-reads the state, and verifies deterministic outcomes.

## Decision-rights model

| Decision or action | Human | Automation |
|---|---:|---:|
| Determine whether content is appropriate | ✓ | |
| Approve claims and disclosures | ✓ | |
| Approve channel copy | ✓ | |
| Authorize publication | ✓ | |
| Retrieve approved content | | ✓ |
| Evaluate encoded governance rules | | ✓ |
| Detect recorded prior publication | | ✓ |
| Execute authorized transaction | | ✓ |
| Record external result | | ✓ |
| Verify deterministic state | | ✓ |
| Resolve ambiguous exceptions | ✓ | |

The goal is not maximum automation. It is **appropriate allocation of work**.

## Operating pattern

```text
Human:
review → approve → authorize

Automation:
retrieve → validate → distribute → record → verify

Human:
handle exceptions / assess outcome
```

## Exception boundary

When platform behavior changes, a connector behaves unexpectedly, a result is ambiguous, or a governance rule fails, the workflow should surface the exception rather than invent new policy.

## Broader applicability

The same boundary can support document release, customer communications, controlled procurement, client onboarding, compliance workflows, data updates, and exception management.

**Automate the repeatable transaction without automating away the accountable decision.**
