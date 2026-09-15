# Lessons Learned

## 1. A working connector is not a governed system

The external publishing action was only one step. The larger engineering problem was determining when publication is allowed, preventing duplicates, separating preview from production, recording resulting state, and verifying that state.

## 2. Approval and execution should be separate

Approved content does not necessarily mean “publish now.” PREVIEW/PUBLISH separation allows inspection and testing without weakening governance.

## 3. Duplicate prevention deserves an independent control

A reusable workflow should assume operators will eventually rerun it. Approval can remain true while a previously published channel becomes ineligible for another publication.

## 4. External success is only half the transaction

An HTTP success response proves that the external service accepted an action. It does not prove that the internal record was updated correctly.

```text
external success
→ capture result
→ update governed state
→ retrieve governed state
→ verify persisted result
```

## 5. Preserve a known-good baseline

Once Company and Founder production paths had successfully distributed the real case study, successful flow copies were preserved before later experimentation. This distinguishes proven behavior from improvement work.

## 6. Channel-specific behavior should not redefine the core engine

Presentation or connector-specific limitations should be addressed as channel improvements where possible instead of continually changing the validated core architecture.

## 7. Transaction success and presentation quality are different

A platform can successfully create a post while the resulting presentation is not yet optimal. Future iterations can improve image prominence and channel-native presentation without changing the governance model.

## 8. Public proof of work requires deliberate sanitization

Operational evidence can expose credentials, tenant details, connector identifiers, repository coordinates, protected payloads, and tracking values. Public documentation should demonstrate the control pattern without exposing unnecessary implementation secrets.

## 9. Metadata can function as operational state

Structured metadata became more valuable when it represented approvals, dependencies, publication intent, channel status, publication references, and lifecycle state.

**Well-designed metadata can coordinate human decisions and automated execution across systems.**

## 10. Governance does not have to eliminate speed

Once human decisions are represented explicitly, automation can perform the mechanical sequence quickly and consistently. The objective is not fewer controls; it is **better placement of controls**.

## Future improvement track

FF-02B v1.0 is intentionally frozen. Future work can separately address larger hero imagery, connector-specific content handling, stronger telemetry, measurement automation, additional channels, retry strategies, and reusable channel-adapter abstractions.
