# Governance Controls

## Objective

> **A workflow that can publish externally should not be allowed to infer its own permission to publish.**

Governance is encoded separately from the publication action.

## 1. Publication authorization

Before execution, the workflow validates governed metadata such as supported schema, overall approval, channel approval, required upstream state, publish intent, and eligible lifecycle status.

Public-safe representation:

```text
ALLOW only when:
  schema is supported
  AND publication is approved
  AND requested channel is approved
  AND required dependencies are satisfied
  AND channel publish flag is enabled
  AND channel status is eligible
```

## 2. Duplicate prevention

A separate gate checks for evidence that the target channel has already been published.

```text
ALLOW only when:
  post URL is empty
  AND published timestamp is empty
```

Approval and duplicate eligibility remain independent controls.

## 3. Approved source retrieval

Channel copy is retrieved from its approved source rather than composed ad hoc inside the external publishing action. This preserves traceability from reviewed copy to executed copy.

## 4. Payload preview

A previewable payload creates an inspection boundary before external execution and supports testing without publication.

## 5. PREVIEW/PUBLISH separation

Production requires an explicit execution mode:

```text
IF execution_mode == "PUBLISH"
    external action may execute
ELSE
    preview path only
```

This is separate from content approval.

## 6. External result capture

After publication, the workflow captures the external result required for state management. Successful production validation included an HTTP `201 Created` response from LinkedIn.

## 7. Governed writeback

The workflow records publication state back to the governed repository. A public-safe example is:

```json
{
  "status": "published",
  "post_url": "<recorded-publication-reference>",
  "published_at": "<timestamp>",
  "last_error": null
}
```

## 8. Post-writeback verification

The workflow retrieves the record again and verifies persisted state against the captured result.

```text
VERIFY:
  lifecycle reflects distribution
  AND channel status == published
  AND stored publication reference == captured reference
  AND stored publication timestamp == captured timestamp
```

## Defense in depth

The system combines approval state, dependencies, duplicate prevention, explicit execution mode, result capture, writeback, and post-writeback verification. No single condition is treated as the entire governance system.

Production expressions, credentials, private repository coordinates, connector identifiers, tenant information, and tracking values are intentionally excluded.
