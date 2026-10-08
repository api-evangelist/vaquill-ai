---
name: vaquill-ai-citation-resolution
description: Resolve a US statutory citation to its exact section and read the governing text, with batch resolution for many citations
api: Vaquill Legal Data API
operations:
- resolve_statute_citation
- resolve_statute_citations_batch
- get_section_api_v1_us_statutes_section__act_id__get
- get_section_body_api_v1_us_statutes_section__act_id__body_get
- get_section_changes_api_v1_us_statutes_section__act_id__changes_get
generated: '2026-10-07'
method: generated
source: openapi/vaquill-ai-openapi.yml; openapi/vaquill-ai-india-openapi.yml; https://www.vaquill.ai/docs/api-guide/alerts; https://www.vaquill.ai/docs/api-guide/pagination; https://www.vaquill.ai/docs/api-guide/errors
---

# Resolve a US statutory citation to its exact section and read the governing text

1. Call `resolve_statute_citation` (GET /api/v1/us/statutes/resolve) with the citation string (for example `42 U.S.C. § 1983` or `17 CFR 240.10b-5`). The verdict is confirmed against the corpus; a citation the corpus cannot name is refused rather than guessed. Costs 2 credits.
2. For many citations call `resolve_statute_citations_batch` (POST /api/v1/us/statutes/resolve) with up to 50 citations; billed 2 per citation.
3. Take the returned `actId` and call `get_section_api_v1_us_statutes_section__act_id__get` for metadata (citation, hierarchy, breadcrumb, status, format links), then `get_section_body_api_v1_us_statutes_section__act_id__body_get` for the full text (6 credits; `format=content`, `structured=true`, `asOf` for point-in-time).
4. When currency matters, call `get_section_changes_api_v1_us_statutes_section__act_id__changes_get` (cursor-paged with `sinceId`/`beforeId`) before asserting the section is unchanged.
5. Read `creditsConsumed` on each response rather than computing cost from the list price.

## Conventions

- Auth: `Authorization: Bearer vq_key_...` (keys from https://app.vaquill.ai/settings).
- Errors: JSON `{"detail": ...}`; 422 carries a `loc` array naming the field.
- Rate limiting: 429 with `Retry-After` seconds; back off exponentially.
- Idempotency: none on the Data API; watches are unique on (board, channel, scope) and a repeat POST answers 409.
