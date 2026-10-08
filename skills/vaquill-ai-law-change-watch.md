---
name: vaquill-ai-law-change-watch
description: Subscribe to a body of law and receive email or HMAC-signed webhook deliveries when it changes, with a test delivery and a per-change diff
api: Vaquill Legal Data API
operations:
- list_boards_api_v1_boards_get
- create_watch_api_v1_watches_post
- test_watch_api_v1_watches__watch_id__test_post
- list_watch_changes_api_v1_watches__watch_id__changes_get
- get_watch_change_diff_api_v1_watches__watch_id__changes__change_id__diff_get
- update_watch_api_v1_watches__watch_id__patch
- delete_watch_api_v1_watches__watch_id__delete
- list_watch_deliveries_api_v1_watches__watch_id__deliveries_get
generated: '2026-10-07'
method: generated
source: openapi/vaquill-ai-openapi.yml; openapi/vaquill-ai-india-openapi.yml; https://www.vaquill.ai/docs/api-guide/alerts; https://www.vaquill.ai/docs/api-guide/pagination; https://www.vaquill.ai/docs/api-guide/errors
---

# Subscribe to a body of law and receive email or HMAC-signed webhook deliveries when it changes

1. Call `list_boards_api_v1_boards_get` (free) to find the board (`corpusType`/`state` pair), its cadence, `lastRetrievedAt`, `retrievalStatus` and whether it is `scopable`.
2. Call `create_watch_api_v1_watches_post` with the board, a `channel` (`email` works on every plan; `webhook` or `both` requires the Business plan and answers 403 otherwise), an optional `scope`, and for webhooks a `webhookUrl`, an optional `webhookSecret` (deliveries are then signed `X-Vaquill-Signature: sha256=<hex>`) and optional `webhookAuth`. A 409 means you already hold this watch on the same board, channel and scope: list watches and reuse it. A 429 means the plan watch cap (3, or 100 on Business).
3. Call `test_watch_api_v1_watches__watch_id__test_post` to fire a one-off `X-Vaquill-Event: board.test` delivery and confirm the receiver.
4. Read what changed with `list_watch_changes_api_v1_watches__watch_id__changes_get` (cursor in `meta.cursor`), and the before/after text with `get_watch_change_diff_api_v1_watches__watch_id__changes__change_id__diff_get` (4 credits, the only paid call in this flow).
5. Dedup on `deliveryId`, which is stable per watch per refresh event. Inspect delivery attempts with `list_watch_deliveries_api_v1_watches__watch_id__deliveries_get`.
6. Pause with `update_watch_api_v1_watches__watch_id__patch` (`isActive: false`, history kept) or remove with `delete_watch_api_v1_watches__watch_id__delete` (no undo).

## Conventions

- Auth: `Authorization: Bearer vq_key_...` (keys from https://app.vaquill.ai/settings).
- Errors: JSON `{"detail": ...}`; 422 carries a `loc` array naming the field.
- Rate limiting: 429 with `Retry-After` seconds; back off exponentially.
- Idempotency: none on the Data API; watches are unique on (board, channel, scope) and a repeat POST answers 409.
