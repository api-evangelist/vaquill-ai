# Vaquill AI

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Vaquill AI is US primary law data infrastructure: a credit-metered Legal Data API over the US Code, the CFR, every state and territory statutory code, regulations, constitutions, court rules, session laws, agency guidance and executive orders (5M+ sections, 54 jurisdictions), a sibling India API over central and state legislation, a Legal Workspace API for driving matters, documents, drafting, review and compliance checks from your own backend, and a hosted MCP server (OAuth or API key) with a local uvx package and a Claude Code plugin. Three OpenAPI 3.1 documents are published on api.vaquill.ai, and the Open US Law corpus is released on GitHub under CC BY-NC 4.0.

**Areas:** Legal · Statutes · Regulations · Legal Research · Law · Compliance · Legal Tech · Government Data · MCP · India · Contracts

## Vaquill AI on APIs.io

Everything profiled for Vaquill AI is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/vaquill-ai/](https://apis.io/providers/vaquill-ai/)** — or go straight to one of the APIs or properties below.

### APIs (26)

- [Vaquill AI Board Watches API](https://apis.io/apis/vaquill-ai/vaquill-ai-board-watches-api/) — Law-change alerts. Subscribe to a **board** (a tracked corpus source, identified by `corpusType` plus an optional `state`) and get a webhook or email…
- [Vaquill AI Chronology API](https://apis.io/apis/vaquill-ai/vaquill-ai-chronology-api/) — The dated events across a matter's documents, as one timeline, with duplicate and date-conflict flags.
- [Vaquill AI Clients API](https://apis.io/apis/vaquill-ai/vaquill-ai-clients-api/) — The people and companies matters are filed under. Synchronous CRUD.
- [Vaquill AI Comparisons API](https://apis.io/apis/vaquill-ai/vaquill-ai-comparisons-api/) — Diffing two documents in a matter into structural changes, with a substantive-versus-cosmetic judgment and a downloadable redline.
- [Vaquill AI Compliance API](https://apis.io/apis/vaquill-ai/vaquill-ai-compliance-api/) — Checking one document against one regulation's requirement checklist: a verdict per requirement with the article it comes from, the gaps, and what to do…
- [Vaquill AI Credits API](https://apis.io/apis/vaquill-ai/vaquill-ai-credits-api/) — Your own credit balance: what is spendable right now, where it came from, and what is about to expire. Free and never charged, so it is safe to poll for…
- [Vaquill AI Documents API](https://apis.io/apis/vaquill-ai/vaquill-ai-documents-api/) — Files in a matter: their metadata, their ingested text, and the original bytes. A document is only usable by retrieval, drafting and review once its status…
- [Vaquill AI Drafting API](https://apis.io/apis/vaquill-ai/vaquill-ai-drafting-api/) — Generating, revising and exporting draft documents. Bodies come out as sections and go in as markdown; the editor's own format is never on the wire.…
- [Vaquill AI Facts API](https://apis.io/apis/vaquill-ai/vaquill-ai-facts-api/) — The cross-document fact ledger for a matter: what every document in it asserts, coalesced and cited back to its source passages.
- [Vaquill AI Folders API](https://apis.io/apis/vaquill-ai/vaquill-ai-folders-api/) — Organization inside and across matters. The same folders the web app shows, so one created here appears in the customer's browser.
- [Vaquill AI India Credits API](https://apis.io/apis/vaquill-ai/vaquill-ai-india-credits-api/) — The India Credits API from Vaquill AI — 1 operation(s) for india credits.
- [Vaquill AI India Pricing API](https://apis.io/apis/vaquill-ai/vaquill-ai-india-pricing-api/) — The India Pricing API from Vaquill AI — 1 operation(s) for india pricing.
- [Vaquill AI Indian Acts and Legislation API](https://apis.io/apis/vaquill-ai/vaquill-ai-indian-acts-and-legislation-api/) — The Indian Acts and Legislation API from Vaquill AI — 17 operation(s) for indian acts and legislation.
- [Vaquill AI Matrices API](https://apis.io/apis/vaquill-ai/vaquill-ai-matrices-api/) — Spreadsheet-style extraction across many documents: rows are documents, columns are questions, cells are answers with verified citations. Building a grid is…
- [Vaquill AI Matter summary API](https://apis.io/apis/vaquill-ai/vaquill-ai-matter-summary-api/) — A citation-backed summary of everything filed to a matter, generated on demand and readable claim by claim.
- [Vaquill AI Matters API](https://apis.io/apis/vaquill-ai/vaquill-ai-matters-api/) — The unit of work everything else hangs off. A matter scopes documents, drafts, reviews, comparisons and matrices, and it is what a credential's access is…
- [Vaquill AI NDA triage API](https://apis.io/apis/vaquill-ai/vaquill-ai-nda-triage-api/) — Screening one inbound NDA against ten standard criteria and, where you name one, your own NDA playbook. Answers `green`, `yellow` or `red` with the…
- [Vaquill AI Operations API](https://apis.io/apis/vaquill-ai/vaquill-ai-operations-api/) — The one job envelope. Every long-running call answers `202` with an operation, and polling this resource is the only way to learn it finished: there are no…
- [Vaquill AI Playbooks API](https://apis.io/apis/vaquill-ai/vaquill-ai-playbooks-api/) — The organization's negotiating positions, per contract type, and the starter templates to build them from. A playbook is the input a contract review is…
- [Vaquill AI Pricing API](https://apis.io/apis/vaquill-ai/vaquill-ai-pricing-api/) — Credit pricing and conversion rates. No authentication required. 1 credit = $0.01 USD.
- [Vaquill AI Research API](https://apis.io/apis/vaquill-ai/vaquill-ai-research-api/) — Asking legal questions and getting grounded, cited answers. This API does NOT stream: an ask answers `202` and you poll the operation, then read the answer…
- [Vaquill AI Reviews API](https://apis.io/apis/vaquill-ai/vaquill-ai-reviews-api/) — Reviewing one contract against a playbook: clause analysis, redlines, flags, liability exposure and a reported sign-off gate. Export applies the redlines as…
- [Vaquill AI Uploads API](https://apis.io/apis/vaquill-ai/vaquill-ai-uploads-api/) — Getting files in. One presigned multipart flow at every size, with the bytes going straight to storage and never through this API. Initiate, PUT each part,…
- [Vaquill AI US Session Laws API](https://apis.io/apis/vaquill-ai/vaquill-ai-us-session-laws-api/) — State session laws: the acts of each legislature as they were enacted, chapter by chapter, before they are folded into a code. A session law is what the…
- [Vaquill AI US Statutes API](https://apis.io/apis/vaquill-ai/vaquill-ai-us-statutes-api/) — Search and retrieve US primary law. Covers the United States Code and the Statutes at Large, the Code of Federal Regulations and its annual editions, state…
- [Vaquill AI Workflows API](https://apis.io/apis/vaquill-ai/vaquill-ai-workflows-api/) — Multi-step analyses from a fixed catalogue. Read a definition to learn what documents and inputs it takes, launch a run inside a matter, then download the…

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Vaquill Ai Webhooks](https://apis.io/asyncapis/vaquill-ai/vaquill-ai-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [Vaquill MCP Server](https://apis.io/servers/vaquill-ai/vaquill-mcp-server/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Vaquill Ai Agentic Access](https://apis.io/agentic-access/vaquill-ai/vaquill-ai-agentic-access/)

#### JSON Schema (18)

The data models the API reads and writes.

- [ActCitedByResponse](https://apis.io/schemas/vaquill-ai/vaquill-ai-act-cited-by-response/)
- [ActSearchRequest](https://apis.io/schemas/vaquill-ai/vaquill-ai-act-search-request/)
- [ActStatusResponse](https://apis.io/schemas/vaquill-ai/vaquill-ai-act-status-response/)
- [ActSubordinateResponse](https://apis.io/schemas/vaquill-ai/vaquill-ai-act-subordinate-response/)
- [ActTextResponse](https://apis.io/schemas/vaquill-ai/vaquill-ai-act-text-response/)
- [AskRequest](https://apis.io/schemas/vaquill-ai/vaquill-ai-ask-request/)
- [ComplianceCheck](https://apis.io/schemas/vaquill-ai/vaquill-ai-compliance-check/)
- [CreateWatchRequest](https://apis.io/schemas/vaquill-ai/vaquill-ai-create-watch-request/)
- [ExternalCreditBalanceResponse](https://apis.io/schemas/vaquill-ai/vaquill-ai-external-credit-balance-response/)
- [Matter](https://apis.io/schemas/vaquill-ai/vaquill-ai-matter/)
- [NdaTriage](https://apis.io/schemas/vaquill-ai/vaquill-ai-nda-triage/)
- [Review](https://apis.io/schemas/vaquill-ai/vaquill-ai-review/)
- [ReviewCreateRequest](https://apis.io/schemas/vaquill-ai/vaquill-ai-review-create-request/)
- [SessionLawBodyResponse](https://apis.io/schemas/vaquill-ai/vaquill-ai-session-law-body-response/)
- [SessionLawResponse](https://apis.io/schemas/vaquill-ai/vaquill-ai-session-law-response/)
- [StatuteBodyResponse](https://apis.io/schemas/vaquill-ai/vaquill-ai-statute-body-response/)
- [StatuteCountRequest](https://apis.io/schemas/vaquill-ai/vaquill-ai-statute-count-request/)
- [StatuteSearchRequest](https://apis.io/schemas/vaquill-ai/vaquill-ai-statute-search-request/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Vaquill Ai Context](https://apis.io/jsonld/vaquill-ai/vaquill-ai-context/)

#### Overlays (3)

OpenAPI overlays, including conversational phrasing for each operation.

- [Vaquill Ai India Overlay](https://apis.io/overlays/vaquill-ai/vaquill-ai-india-overlay/)
- [Vaquill Ai Openapi Overlay](https://apis.io/overlays/vaquill-ai/vaquill-ai-openapi-overlay/)
- [Vaquill Ai Workspace Overlay](https://apis.io/overlays/vaquill-ai/vaquill-ai-workspace-overlay/)

#### Governance rules (1)

Spectral rulesets for the provider's contracts.

- [Vaquill AI API Rules](https://apis.io/rules/vaquill-ai/vaquill-ai-rules/)

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Vaquill Ai Authentication](https://apis.io/security/vaquill-ai/vaquill-ai-authentication/)
- [Vaquill Ai Domain Security](https://apis.io/security/vaquill-ai/vaquill-ai-domain-security/)
- [Vaquill Ai Trust Center](https://apis.io/security/vaquill-ai/vaquill-ai-trust-center/)
- [Vaquill Ai Vulnerability Disclosure](https://apis.io/security/vaquill-ai/vaquill-ai-vulnerability-disclosure/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Vaquill Ai Scopes](https://apis.io/scopes/vaquill-ai/vaquill-ai-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Vaquill Ai Plans Pricing](https://apis.io/plans/vaquill-ai/vaquill-ai-plans-pricing/)

#### Rate limits (2)

Published request limits.

- [Vaquill Ai Rate Limits](https://apis.io/rate-limits/vaquill-ai/vaquill-ai-rate-limits/)
- [Vaquill Ai Workspace Rate Limits](https://apis.io/rate-limits/vaquill-ai/vaquill-ai-workspace-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.vaquill.ai)
- [Documentation](https://www.vaquill.ai/docs/introduction)
- [Getting started](https://www.vaquill.ai/docs/api-guide/quickstart)
- [API reference](https://www.vaquill.ai/docs/api-reference/us-statutes/search-us-statutes-constitutions-court-rules-and-executive-actions)
- [Pricing](https://www.vaquill.ai/pricing)
- [Sign up](https://app.vaquill.ai/auth/signup)
- [Support](https://www.vaquill.ai/support)
- [Changelog](https://www.vaquill.ai/docs/api-guide/changelog)
- [Blog](https://www.vaquill.ai/blog)
- [Security](https://www.vaquill.ai/security)
- [Terms of service](https://www.vaquill.ai/terms)
- [Privacy policy](https://www.vaquill.ai/privacy)
- [GitHub](https://github.com/Vaquill-AI)

## API Evangelist rating

**Kin Score 71.6** — exemplar · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 80.0 |
| Contract quality | 74.3 |
| Contract governance | 22.0 |
| Operational transparency | 68.4 |
| Developer ergonomics | 73.2 |
| Access clarity | 73.7 |

**Agent readiness 67.0** — agent-native

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | verified |
| MCP Server | documented (partial credit) |
| Auth Clarity | served (partial credit) |
| Idempotency | verified |
| Error Semantics | verified |
| OpenAPI Examples | verified |
| Rate Limit Signal | verified |
| Event Surface Described | yes |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | — |
| Dynamic Client Registration | yes |
| Agentic Commerce | — |
| Pagination Ratio | paginated |
| Operation Distinctiveness | distinct |

**Regulatory alignment 45.1** — Government & Public Sector

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/vaquill-ai/](https://apis.io/providers/vaquill-ai/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Vaquill AI: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/vaquill-ai/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
