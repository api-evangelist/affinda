# Affinda (affinda)
Affinda is an Intelligent Document Processing (IDP) platform that uses AI to extract structured data from documents — resumes, invoices, receipts, contracts, passports, identity documents, and custom document types — with confidence scores, bounding boxes, and OCR output. The v3 REST API exposes document upload and parsing, document type configuration, workspaces, collections, data sources for master-data matching, validation results, annotations for human-in-the-loop review, resthook-style webhooks, daily credits usage reporting, and resume / job-description search and match. Affinda is deployed across AUS/Global, US, and EU regions for data residency, holds SOC 2 Type II and ISO 27001:2022, and ships official Python, TypeScript, .NET, and Java SDKs alongside a `skill.md` file built for AI coding agents.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/affinda/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

 - AI, Artificial Intelligence, Document Processing, Intelligent Document Processing, IDP, OCR, Resume Parsing, Invoice Parsing, Receipt Parsing, Document Extraction, Document Classification, Document Splitting, Recruitment, Banking, Insurance, Logistics, Healthcare, Government

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## Regions

| Region | API Base URL | App URL |
|---|---|---|
| AUS / Global | `https://api.affinda.com` | `https://app.affinda.com` |
| United States | `https://api.us1.affinda.com` | `https://app.us1.affinda.com` |
| European Union | `https://api.eu1.affinda.com` | `https://app.eu1.affinda.com` |

Authentication is via Bearer token. Generate per-user API keys in the dashboard under Settings -> API Keys (max 3 active keys per user).

## APIs

### Affinda Documents API
Upload documents (PDF, DOC, DOCX, XLSX, ODT, RTF, TXT, HTML, PNG, JPG, JPEG, TIFF) and receive structured JSON extraction with confidence scores, bounding boxes, and OCR text. Default file-size cap is 20 MB (5 MB for resumes), 20 pages per document.

**Human URL:** [https://docs.affinda.com/reference/getting-started](https://docs.affinda.com/reference/getting-started)

- [OpenAPI](openapi/affinda-documents-api-openapi.yml)
- [JSON Schema — Document](json-schema/affinda-document-schema.json)
- [JSON-LD](json-ld/affinda-context.jsonld)
- [Naftiko Capability — Documents](capabilities/documents-documents.yaml)

### Affinda Document Types API
Manage document type definitions — the model configuration governing how a specific document category (invoice, resume, contract, custom) is parsed. Each type exposes a JSON Schema and Pydantic model.

- [OpenAPI](openapi/affinda-document-types-api-openapi.yml)
- [Naftiko Capability — Document Types](capabilities/document-types-document-types.yaml)

### Affinda Extractors API
List and inspect the underlying extractor models that power document parsing (resume, invoice, receipt, passport, etc.).

- [OpenAPI](openapi/affinda-extractors-api-openapi.yml)

### Affinda Document Splitters API
Configure document splitting and classification across multi-document PDFs. Splitters detect boundaries, classify each segment, and route to the correct extractor.

- [OpenAPI](openapi/affinda-document-splitters-api-openapi.yml)

### Affinda Workspaces API
Workspaces group collections, documents, members, and webhook subscriptions, and scope every document upload and listing. Includes per-workspace usage reporting.

- [OpenAPI](openapi/affinda-workspaces-api-openapi.yml)
- [Naftiko Capability — Workspaces](capabilities/workspaces-workspaces.yaml)

### Affinda Organizations API
Read and update the top-level organization account. Organizations contain users, billing, document types, and workspaces.

- [OpenAPI](openapi/affinda-organizations-api-openapi.yml)

### Affinda Invitations API
Create, list, and respond to invitations. Supports invitation token lookup and revocation.

- [OpenAPI](openapi/affinda-invitations-api-openapi.yml)

### Affinda Data Sources API
Manage custom mapping data sources — master-data lists used to match raw extracted values (vendor names, SKUs, categories) to canonical entities during parsing.

- [OpenAPI](openapi/affinda-data-sources-api-openapi.yml)
- [Naftiko Capability — Data Sources](capabilities/data-sources-data-sources.yaml)

### Affinda Annotations API
Manually create, update, and delete field-level annotations on parsed documents — the surface for human-in-the-loop validation and review. Supports batch create, update, and delete.

- [OpenAPI](openapi/affinda-annotations-api-openapi.yml)
- [JSON Schema — Annotation](json-schema/affinda-annotation-schema.json)
- [Naftiko Capability — Annotations](capabilities/annotations-annotations.yaml)

### Affinda Validation Results API
Track validation-rule status and findings on parsed documents. Drives the embeddable validation UI. Supports batch operations.

- [OpenAPI](openapi/affinda-validation-results-api-openapi.yml)

### Affinda Tags API
Tag parsed documents for routing, segmentation, search filtering, and workflow triggers. Supports batch-add and batch-remove on document collections.

- [OpenAPI](openapi/affinda-tags-api-openapi.yml)

### Affinda Usage API
Retrieve daily credits consumption for the organization across all workspaces and document types. Use for billing reconciliation, budget tracking, and FinOps reporting.

- [OpenAPI](openapi/affinda-usage-api-openapi.yml)

### Affinda Webhooks API
Resthook-style webhook subscriptions for document parsing events. Create a subscription, receive a probe, and activate to confirm the receiver. Events include document parsed, failed, and validated.

- [OpenAPI](openapi/affinda-webhooks-api-openapi.yml)
- [Naftiko Capability — Webhooks](capabilities/webhooks-webhooks.yaml)

### Affinda Search and Match API
Resume search, job description search, and matching across parsed-document indexes. Score candidates against a job description (or vice versa), retrieve match details, configure search and embed parameters, and request job-title and skill suggestions. Includes index management for organizing parsed documents.

- [OpenAPI](openapi/affinda-search-match-api-openapi.yml)
- [Naftiko Capability — Resume Search](capabilities/search-match-resume-search.yaml)
- [Naftiko Capability — Job Description Search](capabilities/search-match-job-description-search.yaml)

## Common Properties

- [Portal](https://www.affinda.com)
- [Documentation](https://docs.affinda.com)
- [API Reference](https://docs.affinda.com/reference)
- [GettingStarted](https://docs.affinda.com/reference/getting-started)
- [Skill File for AI Agents](https://docs.affinda.com/skill.md)
- [OpenAPI Spec (v3)](https://api.affinda.com/static/v3/api_spec.yaml)
- [Pricing](https://www.affinda.com/pricing)
- [SignUp](https://app.affinda.com/auth/register)
- [Login (AUS/Global)](https://app.affinda.com/auth/login)
- [Login (US)](https://app.us1.affinda.com/auth/login)
- [Login (EU)](https://app.eu1.affinda.com/auth/login)
- [Authentication](https://docs.affinda.com/reference/authentication)
- [Webhooks Guide](https://docs.affinda.com/reference/webhooks)
- [ChangeLog](https://docs.affinda.com/changelog)
- [Blog](https://www.affinda.com/blog)
- [Academy](https://www.affinda.com/affinda-academy)
- [Support](https://support.affinda.com)
- [Security](https://www.affinda.com/security)
- [Terms of Service](https://www.affinda.com/legal/terms-of-use)
- [Privacy Policy](https://www.affinda.com/legal/privacy-policy)
- [GitHub Organization](https://github.com/affinda)
- [LinkedIn](https://www.linkedin.com/company/affinda)
- [Twitter / X](https://twitter.com/affinda_ai)
- [SDK — Python](https://github.com/affinda/affinda-python) ([PyPI](https://pypi.org/project/affinda/))
- [SDK — TypeScript](https://github.com/affinda/affinda-typescript) ([NPM](https://www.npmjs.com/package/@affinda/affinda))
- [SDK — .NET (Affinda.API)](https://www.nuget.org/packages/Affinda.API)
- [SDK — Java (com.affinda.api:affinda-api-client)](https://central.sonatype.com/artifact/com.affinda.api/affinda-api-client)

## Compliance

- SOC 2 Type II
- ISO 27001:2022
- GDPR
- HIPAA (Enterprise tier)

## Artifacts

Machine-readable specifications and supporting artifacts organized by format.

### OpenAPI

- [Affinda v3 (full spec)](openapi/affinda-v3-openapi.yml)
- [Affinda Documents API](openapi/affinda-documents-api-openapi.yml)
- [Affinda Document Types API](openapi/affinda-document-types-api-openapi.yml)
- [Affinda Extractors API](openapi/affinda-extractors-api-openapi.yml)
- [Affinda Document Splitters API](openapi/affinda-document-splitters-api-openapi.yml)
- [Affinda Workspaces API](openapi/affinda-workspaces-api-openapi.yml)
- [Affinda Organizations API](openapi/affinda-organizations-api-openapi.yml)
- [Affinda Invitations API](openapi/affinda-invitations-api-openapi.yml)
- [Affinda Data Sources API](openapi/affinda-data-sources-api-openapi.yml)
- [Affinda Annotations API](openapi/affinda-annotations-api-openapi.yml)
- [Affinda Validation Results API](openapi/affinda-validation-results-api-openapi.yml)
- [Affinda Tags API](openapi/affinda-tags-api-openapi.yml)
- [Affinda Usage API](openapi/affinda-usage-api-openapi.yml)
- [Affinda Webhooks API](openapi/affinda-webhooks-api-openapi.yml)
- [Affinda Search and Match API](openapi/affinda-search-match-api-openapi.yml)

### JSON Schema

- [Affinda Document Schema](json-schema/affinda-document-schema.json)
- [Affinda Annotation Schema](json-schema/affinda-annotation-schema.json)
- [Affinda Resume Schema](json-schema/affinda-resume-schema.json)
- [Affinda Invoice Schema](json-schema/affinda-invoice-schema.json)

### JSON-LD

- [Affinda Context](json-ld/affinda-context.jsonld)

### Naftiko Capabilities

- [Documents](capabilities/documents-documents.yaml)
- [Document Types](capabilities/document-types-document-types.yaml)
- [Workspaces](capabilities/workspaces-workspaces.yaml)
- [Data Sources](capabilities/data-sources-data-sources.yaml)
- [Annotations](capabilities/annotations-annotations.yaml)
- [Webhooks](capabilities/webhooks-webhooks.yaml)
- [Resume Search](capabilities/search-match-resume-search.yaml)
- [Job Description Search](capabilities/search-match-job-description-search.yaml)

### Examples

- [Upload Document](examples/affinda-upload-document-example.json)
- [Get Parsed Resume](examples/affinda-get-parsed-resume-example.json)
- [Resume Search](examples/affinda-resume-search-example.json)
- [Webhook Subscription](examples/affinda-webhook-subscription-example.json)

### Spectral Rules

- [Affinda Spectral Ruleset](rules/affinda-rules.yml)

### Vocabulary

- [Affinda Vocabulary](vocabulary/affinda-vocabulary.yml)

### Plans, Rate Limits, and FinOps

- [Plans and Pricing](plans/affinda-plans-pricing.yml)
- [Rate Limits](rate-limits/affinda-rate-limits.yml)
- [FinOps Definition](finops/affinda-finops.yml)
