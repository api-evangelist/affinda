# Affinda

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

Affinda is an Intelligent Document Processing (IDP) platform that uses AI to extract structured data from documents — resumes, invoices, receipts, contracts, passports, IDs, and custom document types. The v3 REST API exposes document upload and parsing, document type configuration, workspaces, collections, data sources for master-data matching, validation results, annotations for human-in-the-loop review, webhooks via resthook subscriptions, daily usage reporting, and resume / job-description search and match for recruitment workflows. The platform is deployed across AUS/Global, US, and EU regions for data residency, holds SOC 2 Type II and ISO 27001:2022 certification, and ships official Python, TypeScript, .NET, and Java SDKs alongside a skill.md file for AI coding agents.

**Areas:** Artificial Intelligence · Document Processing · Intelligent Document Processing · OCR · Resume Parsing · Invoice Parsing · Receipt Parsing · Document Extraction · Document Classification · Document Splitting · Recruiting · Banking

## Affinda on APIs.io

Everything profiled for Affinda is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/affinda/](https://apis.io/providers/affinda/)** — or go straight to one of the APIs or properties below.

### APIs (16)

- [Affinda Documents API](https://apis.io/apis/affinda/affinda-documents-api/) — Upload documents (PDF, images, DOCX, XLSX, TXT, HTML) and Affinda returns structured JSON extraction with confidence scores, bounding boxes, and OCR text.…
- [Affinda Document Types API](https://apis.io/apis/affinda/affinda-document-types-api/) — Manage document type definitions — the model configuration governing how a specific document category (invoice, resume, custom contract) is parsed. Each…
- [Affinda Workspaces API](https://apis.io/apis/affinda/affinda-workspaces-api/) — Workspaces group together related collections, documents, members, and webhook subscriptions. Workspace identifiers scope every document upload, listing,…
- [Affinda Organizations API](https://apis.io/apis/affinda/affinda-organizations-api/) — Manage the top-level organization account — read and update organization details. Organizations contain users, billing, document types, and workspaces.…
- [Affinda Data Sources API](https://apis.io/apis/affinda/affinda-data-sources-api/) — Manage custom mapping data sources — master-data lists used to match raw extracted values (vendor names, SKUs, categories) to known canonical entities.…
- [Affinda Annotations API](https://apis.io/apis/affinda/affinda-annotations-api/) — Manually create, update, and delete annotations on uploaded documents. Annotations are the field-level extraction objects (value, confidence, bounding box,…
- [Affinda Validation Results API](https://apis.io/apis/affinda/affinda-validation-results-api/) — Track the status and findings of validation rules attached to parsed documents. Validation results record passes, failures, and remediation context for…
- [Affinda Tags API](https://apis.io/apis/affinda/affinda-tags-api/) — Tag management for parsed documents. Tags can be arbitrarily attached to documents to support routing, segmentation, search filters, and downstream workflow…
- [Affinda Usage API](https://apis.io/apis/affinda/affinda-usage-api/) — Retrieve daily credits consumption for the organization across all workspaces and document types. Used for billing reconciliation, budget tracking, and…
- [Affinda Webhooks API](https://apis.io/apis/affinda/affinda-webhooks-api/) — Resthook-style webhook subscriptions for document parsing events. Create a subscription, receive a probe payload, and call the activation endpoint to…
- [Affinda Search and Match API](https://apis.io/apis/affinda/affinda-search-match-api/) — Resume search, job description search, and matching across parsed-document indexes. Score candidates against a job description (or vice versa), retrieve…
- [Affinda Add x-hidden to endpoints API](https://apis.io/apis/affinda/affinda-add-x-hidden-to-endpoints-api/) — Hidden endpoints not intended for public use. These endpoints include Splitting, Extractor, Organization, and Workspace Memberships & Usage functionality.
- [Affinda Deprecated End Points API](https://apis.io/apis/affinda/affinda-deprecated-end-points-api/) — Deprecated endpoints that are maintained for backward compatibility. These endpoints include Data Point, Collection, and Users functionality that has been…
- [Affinda Document API - Extractor API](https://apis.io/apis/affinda/affinda-document-api-extractor-api/) — The Document API - Extractor API from Affinda — 2 operation(s) for document api - extractor.
- [Affinda Document API - Splitting API](https://apis.io/apis/affinda/affinda-document-api-splitting-api/) — The Document API - Splitting API from Affinda — 3 operation(s) for document api - splitting.
- [Affinda Organization API - Invitation API](https://apis.io/apis/affinda/affinda-organization-api-invitation-api/) — The Organization API - Invitation API from Affinda — 3 operation(s) for organization api - invitation.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Arazzo workflows (27)

Multi-step workflows that chain operations into a business task.

- [Affinda Add a Data Field to a Collection](https://apis.io/arazzos/affinda/affinda-add-collection-data-field-workflow/)
- [Affinda Add a Member to a Workspace](https://apis.io/arazzos/affinda/affinda-add-workspace-member-workflow/)
- [Affinda Bootstrap Organization and Workspace](https://apis.io/arazzos/affinda/affinda-bootstrap-organization-workspace-workflow/)
- [Affinda Configure and Embed Resume Search](https://apis.io/arazzos/affinda/affinda-configure-resume-search-embed-workflow/)
- [Affinda Create Enum Data Point and Populate Choices](https://apis.io/arazzos/affinda/affinda-create-data-point-with-choices-workflow/)
- [Affinda Create Mapping Data Source and Add a Value](https://apis.io/arazzos/affinda/affinda-create-data-source-and-add-value-workflow/)
- [Affinda Create Document from Data and Index It](https://apis.io/arazzos/affinda/affinda-create-document-from-data-and-index-workflow/)
- [Affinda Create Extractor with a Data Point](https://apis.io/arazzos/affinda/affinda-create-extractor-with-data-point-workflow/)
- [Affinda Create Search Index and Add a Document](https://apis.io/arazzos/affinda/affinda-create-index-and-add-document-workflow/)
- [Affinda Create a Tag and Apply It to Documents](https://apis.io/arazzos/affinda/affinda-create-tag-and-tag-documents-workflow/)
- [Affinda Create Document Type and Generate JSON Schema](https://apis.io/arazzos/affinda/affinda-document-type-to-json-schema-workflow/)
- [Affinda Find a Document and Move It to Another Collection](https://apis.io/arazzos/affinda/affinda-find-and-move-document-workflow/)
- [Affinda Invite Organization Member and Respond](https://apis.io/arazzos/affinda/affinda-invite-member-and-respond-workflow/)
- [Affinda Job Description Search and Detail](https://apis.io/arazzos/affinda/affinda-job-description-search-and-detail-workflow/)
- [Affinda Parse and Correct Annotations](https://apis.io/arazzos/affinda/affinda-parse-and-correct-annotations-workflow/)
- [Affinda Parse and Reject a Document](https://apis.io/arazzos/affinda/affinda-parse-and-reject-document-workflow/)
- [Affinda Parse and Record a Validation Result](https://apis.io/arazzos/affinda/affinda-parse-and-validate-rule-workflow/)
- [Affinda Provision Collection and Ingest a Document](https://apis.io/arazzos/affinda/affinda-provision-and-ingest-document-workflow/)
- [Affinda Provision Workspace and Collection](https://apis.io/arazzos/affinda/affinda-provision-workspace-collection-workflow/)
- [Affinda Rename Document Type and Refresh Its Schema](https://apis.io/arazzos/affinda/affinda-rename-document-type-and-refresh-schema-workflow/)
- [Affinda Resume Search and Detail](https://apis.io/arazzos/affinda/affinda-resume-search-and-detail-workflow/)
- [Affinda Split a Document and Re-parse](https://apis.io/arazzos/affinda/affinda-split-document-and-reparse-workflow/)
- [Affinda Update Resume Data and Re-index](https://apis.io/arazzos/affinda/affinda-update-resume-data-and-reindex-workflow/)
- [Affinda Upload and Parse a Document](https://apis.io/arazzos/affinda/affinda-upload-and-parse-document-workflow/)
- [Affinda Upload from URL, Parse, and Confirm](https://apis.io/arazzos/affinda/affinda-upload-from-url-and-validate-workflow/)
- …and 2 more published on APIs.io

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [affinda](https://apis.io/servers/affinda/affinda/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Affinda Agentic Access](https://apis.io/agentic-access/affinda/affinda-agentic-access/)

#### JSON Schema (4)

The data models the API reads and writes.

- [Affinda Annotation](https://apis.io/schemas/affinda/affinda-annotation/)
- [Affinda Document](https://apis.io/schemas/affinda/affinda-document/)
- [Affinda Invoice](https://apis.io/schemas/affinda/affinda-invoice/)
- [Affinda Resume](https://apis.io/schemas/affinda/affinda-resume/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Affinda Context](https://apis.io/jsonld/affinda/affinda-context/)

#### Vocabulary (1)

The provider's domain terms, defined.

- [Affinda Vocabulary](https://apis.io/vocabularies/affinda/affinda-vocabulary/)

#### Examples (4)

Example requests and responses.

- [Affinda Get Parsed Resume Example](https://apis.io/examples/affinda/affinda-get-parsed-resume-example/)
- [Affinda Resume Search Example](https://apis.io/examples/affinda/affinda-resume-search-example/)
- [Affinda Upload Document Example](https://apis.io/examples/affinda/affinda-upload-document-example/)
- [Affinda Webhook Subscription Example](https://apis.io/examples/affinda/affinda-webhook-subscription-example/)

#### Collections (34)

Postman and Open Collection request collections.

- [Affinda Annotations Add x-hidden to endpoints API](https://apis.io/collections/affinda/open-affinda-add-x-hidden-to-endpoints-api/)
- [Affinda Add x-hidden to endpoints Annotations API](https://apis.io/collections/affinda/open-affinda-annotations-api/)
- [Affinda Annotations Add x-hidden to endpoints Data Sources API](https://apis.io/collections/affinda/open-affinda-data-sources-api/)
- [Affinda Annotations Add x-hidden to endpoints Deprecated End Points API](https://apis.io/collections/affinda/open-affinda-deprecated-end-points-api/)
- [Affinda Annotations Add x-hidden to endpoints Document API - Extractor API](https://apis.io/collections/affinda/open-affinda-document-api-extractor-api/)
- [Affinda Annotations Add x-hidden to endpoints Document API - Splitting API](https://apis.io/collections/affinda/open-affinda-document-api-splitting-api/)
- [Affinda Document Splitters API](https://apis.io/collections/affinda/open-affinda-document-splitters-api/)
- [Affinda Annotations Add x-hidden to endpoints Document Types API](https://apis.io/collections/affinda/open-affinda-document-types-api/)
- [Affinda Annotations Add x-hidden to endpoints Documents API](https://apis.io/collections/affinda/open-affinda-documents-api/)
- [Affinda Extractors API](https://apis.io/collections/affinda/open-affinda-extractors-api/)
- [Affinda Invitations API](https://apis.io/collections/affinda/open-affinda-invitations-api/)
- [Affinda Annotations Add x-hidden to endpoints Organization API - Invitation API](https://apis.io/collections/affinda/open-affinda-organization-api-invitation-api/)
- [Affinda Annotations Add x-hidden to endpoints Organizations API](https://apis.io/collections/affinda/open-affinda-organizations-api/)
- [Affinda Annotations Add x-hidden to endpoints Search & Match API](https://apis.io/collections/affinda/open-affinda-search-match-api/)
- [Affinda Annotations Add x-hidden to endpoints Tags API](https://apis.io/collections/affinda/open-affinda-tags-api/)
- [Affinda Annotations Add x-hidden to endpoints Usage API](https://apis.io/collections/affinda/open-affinda-usage-api/)
- [Affinda API](https://apis.io/collections/affinda/open-affinda-v3/)
- [Affinda Annotations Add x-hidden to endpoints Validation Results API](https://apis.io/collections/affinda/open-affinda-validation-results-api/)
- [Affinda Annotations Add x-hidden to endpoints Webhooks API](https://apis.io/collections/affinda/open-affinda-webhooks-api/)
- [Affinda Annotations Add x-hidden to endpoints Workspaces API](https://apis.io/collections/affinda/open-affinda-workspaces-api/)
- [Affinda Annotations API](https://apis.io/collections/affinda/postman-affinda-annotations-api/)
- [Affinda Data Sources API](https://apis.io/collections/affinda/postman-affinda-data-sources-api/)
- [Affinda Document Splitters API](https://apis.io/collections/affinda/postman-affinda-document-splitters-api/)
- [Affinda Document Types API](https://apis.io/collections/affinda/postman-affinda-document-types-api/)
- [Affinda Documents API](https://apis.io/collections/affinda/postman-affinda-documents-api/)
- …and 9 more published on APIs.io

#### Governance rules (2)

Spectral rulesets for the provider's contracts.

- [Affinda — jsonschema rules](https://apis.io/rules/affinda/affinda-jsonschema-spectral-rules/)
- [Affinda API Rules](https://apis.io/rules/affinda/affinda-rules/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Affinda Authentication](https://apis.io/security/affinda/affinda-authentication/)
- [Affinda Domain Security](https://apis.io/security/affinda/affinda-domain-security/)
- [Affinda Trust Center](https://apis.io/security/affinda/affinda-trust-center/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Affinda Plans Pricing](https://apis.io/plans/affinda/affinda-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Affinda Rate Limits](https://apis.io/rate-limits/affinda/affinda-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Affinda Finops](https://apis.io/finops/affinda/affinda-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.affinda.com/)
- [Documentation](https://docs.affinda.com)
- [Getting started](https://docs.affinda.com/reference/getting-started)
- [API reference](https://docs.affinda.com/reference)
- [Pricing](https://www.affinda.com/pricing)
- [Support](https://support.affinda.com)
- [Changelog](https://docs.affinda.com/changelog)
- [Blog](https://www.affinda.com/blog)
- [Security](https://www.affinda.com/security)
- [Terms of service](https://www.affinda.com/legal/terms-of-use)
- [Privacy policy](https://www.affinda.com/legal/privacy-policy)
- [GitHub](https://github.com/affinda)

## API Evangelist rating

**Kin Score 54.5** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 65.0 |
| Contract quality | 63.5 |
| Contract governance | 13.6 |
| Operational transparency | 42.1 |
| Developer ergonomics | 79.0 |
| Access clarity | 48.7 |

**Agent readiness 51.5** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | verified |
| Auth Clarity | served (partial credit) |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | partial |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | unknown |
| Agent Skills | unknown |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | verified |
| Dynamic Client Registration | yes |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | distinct |

**Regulatory alignment 18.0** — Insurance

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/affinda/](https://apis.io/providers/affinda/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Affinda: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/affinda/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
