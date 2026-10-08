---
name: vaquill-ai-india-act-lookup
description: Search Indian central and state legislation, resolve a citation to a provision, read its text and amendment history
api: Vaquill India API
operations:
- list_act_filters_api_v1_in_acts_filters_get
- search_acts_api_v1_in_acts_search_post
- resolve_india_citation
- get_act_section_body_api_v1_in_acts__act_id__sections__section_number__body_get
- get_act_amendments_api_v1_in_acts__act_id__amendments_get
- get_act_status_api_v1_in_acts__act_id__status_get
generated: '2026-10-07'
method: generated
source: openapi/vaquill-ai-openapi.yml; openapi/vaquill-ai-india-openapi.yml; https://www.vaquill.ai/docs/api-guide/alerts; https://www.vaquill.ai/docs/api-guide/pagination; https://www.vaquill.ai/docs/api-guide/errors
---

# Search Indian central and state legislation

1. Call `list_act_filters_api_v1_in_acts_filters_get` (free) for the filter vocabulary, then `search_acts_api_v1_in_acts_search_post` (2 credits) for semantic search across central and state enactments.
2. For a known citation call `resolve_india_citation` (GET /api/v1/in/acts/resolve) to land on the exact provision.
3. Read the provision with `get_act_section_body_api_v1_in_acts__act_id__sections__section_number__body_get` and its history with `get_act_amendments_api_v1_in_acts__act_id__amendments_get` (substitutions, insertions, omissions).
4. Before relying on an act, call `get_act_status_api_v1_in_acts__act_id__status_get` to learn whether it is still law and who says so.
5. The same `vq_key_` works here; the India MCP mount is separate (`https://mcp.vaquill.ai/in/s/_`).

## Conventions

- Auth: `Authorization: Bearer vq_key_...` (keys from https://app.vaquill.ai/settings).
- Errors: JSON `{"detail": ...}`; 422 carries a `loc` array naming the field.
- Rate limiting: 429 with `Retry-After` seconds; back off exponentially.
- Idempotency: none on the Data API; watches are unique on (board, channel, scope) and a repeat POST answers 409.
