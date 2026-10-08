---
name: vaquill-ai-statute-search
description: Search US statutes, regulations, constitutions and court rules across 54 jurisdictions, page the ranked results, and pull full text
api: Vaquill Legal Data API
operations:
- list_statutes_coverage_api_v1_us_statutes_coverage_get
- search_statutes_api_v1_us_statutes_search_post
- get_section_body_api_v1_us_statutes_section__act_id__body_get
- get_section_neighbors_api_v1_us_statutes_section__act_id__related_get
- get_section_cross_state_api_v1_us_statutes_section__act_id__cross_state_get
generated: '2026-10-07'
method: generated
source: openapi/vaquill-ai-openapi.yml; openapi/vaquill-ai-india-openapi.yml; https://www.vaquill.ai/docs/api-guide/alerts; https://www.vaquill.ai/docs/api-guide/pagination; https://www.vaquill.ai/docs/api-guide/errors
---

# Search US statutes

1. Call `list_statutes_coverage_api_v1_us_statutes_coverage_get` first (free) to learn which `corpusType` and `state` values exist, and treat an empty result as an absence only after checking it.
2. Call `search_statutes_api_v1_us_statutes_search_post` (POST /api/v1/us/statutes/search, 4 credits) with `query` plus filters (`corpusType`, `state`, `code`, `source`, status, year). Page with `limit` (1-50, default 10) and `offset` (0-70); stop when `hasMore` is false. `count` is per page; there is no corpus-wide total, and `total` is a deprecated alias for `count`.
3. A nonsense query still returns rows: vector search always returns nearest neighbours, so judge relevance from the text, never from the presence of results.
4. For each hit call `get_section_body_api_v1_us_statutes_section__act_id__body_get` for the full text, or set `includeBody` on the search to inline it (adds the body price per row that returns text).
5. Use `get_section_neighbors_api_v1_us_statutes_section__act_id__related_get` for the sections before and after, and `get_section_cross_state_api_v1_us_statutes_section__act_id__cross_state_get` to compare the provision against other states (at most one per state).
6. On 429 honor `Retry-After`; on 402 the account is out of credits.

## Conventions

- Auth: `Authorization: Bearer vq_key_...` (keys from https://app.vaquill.ai/settings).
- Errors: JSON `{"detail": ...}`; 422 carries a `loc` array naming the field.
- Rate limiting: 429 with `Retry-After` seconds; back off exponentially.
- Idempotency: none on the Data API; watches are unique on (board, channel, scope) and a repeat POST answers 409.
