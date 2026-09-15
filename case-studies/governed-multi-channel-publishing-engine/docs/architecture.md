# Architecture

## Purpose

The engine turns an approved content package into a controlled publication transaction without allowing the automation layer to become the publication authority.

## Logical architecture

```text
Governed Content Repository
          |
          v
Decode / Parse Metadata
          |
          v
Publication Authorization
          |
          v
Duplicate Prevention
          |
          v
Approved Channel Copy
          |
          v
Publication Payload Preview
          |
          v
Execution Authorization
     /             \
 PUBLISH          PREVIEW
    |                |
    v                v
External Publish   No publication
    |
    v
Capture Publication Result
    |
    v
Build Updated Metadata
    |
    v
Governed Repository Writeback
    |
    v
Re-read Updated State
    |
    v
Verify Publication State
```

## Core components

### Governed repository

The repository stores content and machine-readable publication metadata representing approvals, channel intent, dependencies, lifecycle state, and publication results. It functions as the system record against which the workflow evaluates eligibility and prior publication.

### Orchestration layer

Microsoft Power Automate retrieves the governed record, parses metadata, evaluates controls, retrieves approved copy, invokes the external connector when authorized, and coordinates writeback and verification.

### Distribution channels

Channel-specific actions sit downstream of governance and execution controls. FF-02B v1.0 validated separate Company and Founder LinkedIn paths.

### Verification loop

The workflow does not stop at connector success. It builds an updated record, writes it back, retrieves it again, parses the persisted version, and verifies that expected publication state is present.

## State model

```text
draft → approved → authorized → ready → distributed → verified
```

A transaction may be blocked at a control boundary because approval is missing, a dependency is unmet, prior publication is detected, execution is PREVIEW, writeback fails, or verified state is inconsistent.

## Architectural principles

**Content state is not execution state.** Approved content does not mean “publish now.”

**API success is not workflow success.** A successful external response does not prove internal state is correct.

**Automation capability is not automation authority.** The workflow can publish technically, but governed human-controlled state determines whether it may.

## Reusability

The pattern supports future channel adapters behind common governance, result-capture, writeback, and verification controls.

The public package intentionally omits production connection names, private endpoints, repository identifiers, and authentication configuration.
