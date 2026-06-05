# Affinda (affinda)

Affinda is an Intelligent Document Processing (IDP) platform that uses AI to extract structured data from documents — resumes, invoices, receipts, contracts, passports, IDs, and custom document types. The v3 REST API exposes document upload and parsing, document type configuration, workspaces, collections, data sources for master-data matching, validation results, annotations for human-in-the-loop review, webhooks via resthook subscriptions, daily usage reporting, and resume / job-description search and match for recruitment workflows. The platform is deployed across AUS/Global, US, and EU regions for data residency, holds SOC 2 Type II and ISO 27001:2022 certification, and ships official Python, TypeScript, .NET, and Java SDKs alongside a skill.md file for AI coding agents.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/affinda/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/affinda/refs/heads/main/apis.yml)

## Scope

- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- AI
- Artificial Intelligence
- Document Processing
- Intelligent Document Processing
- IDP
- OCR
- Resume Parsing
- Invoice Parsing
- Receipt Parsing
- Document Extraction
- Document Classification
- Document Splitting
- Recruitment
- Banking
- Insurance
- Logistics
- Healthcare
- Government

## Timestamps

- **Created:** 2026-05-25T00:00:00.000Z
- **Modified:** 2026-05-25

## APIs

### Affinda Documents API

Upload documents (PDF, images, DOCX, XLSX, TXT, HTML) and Affinda returns structured JSON extraction with confidence scores, bounding boxes, and OCR text. Supports invoices, resumes, receipts, contracts, passports, and custom document types. 20 MB file size limit (5 MB for resumes), 20 pages default. Returns parsing status, raw text, parsed fields, and original file references.

- **Human URL:** [https://docs.affinda.com/reference/getting-started](https://docs.affinda.com/reference/getting-started)

#### Tags

- Document Processing
- Document Extraction
- AI
- OCR

#### Properties

- [Documentation](https://docs.affinda.com/reference/getting-started)
- [OpenAPI](openapi/affinda-documents-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/affinda-documents-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/affinda-documents-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/affinda-document-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/affinda-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

### Affinda Document Types API

Manage document type definitions — the model configuration governing how a specific document category (invoice, resume, custom contract) is parsed. Each document type exposes a JSON Schema and optional Pydantic model representation. Document types are configured in the dashboard or natural-language workflow builder and reused across workspaces and collections.

- **Human URL:** [https://docs.affinda.com/reference/document-types](https://docs.affinda.com/reference/document-types)

#### Tags

- Document Processing
- Document Types
- Models
- Configuration

#### Properties

- [Documentation](https://docs.affinda.com/reference/document-types)
- [OpenAPI](openapi/affinda-document-types-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/affinda-document-types-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/affinda-document-types-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Affinda Extractors API

List and inspect the underlying extractor models that power document parsing. Extractors are Affinda's named ML pipelines (resume extractor, invoice extractor, receipt extractor, passport extractor, etc.) and are referenced from document type configurations.

- **Human URL:** [https://docs.affinda.com/reference](https://docs.affinda.com/reference)

#### Tags

- Document Processing
- Extractors
- Models

#### Properties

- [Documentation](https://docs.affinda.com/reference)
- [OpenAPI](openapi/affinda-extractors-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/affinda-extractors-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/affinda-extractors-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Affinda Document Splitters API

Configure and run document splitting and classification across multi-document PDFs. Splitters identify document boundaries inside a single uploaded file, classify each segment by document type, and route each segment to the correct extractor.

- **Human URL:** [https://docs.affinda.com/reference](https://docs.affinda.com/reference)

#### Tags

- Document Processing
- Splitting
- Classification

#### Properties

- [Documentation](https://docs.affinda.com/reference)
- [OpenAPI](openapi/affinda-document-splitters-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/affinda-document-splitters-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/affinda-document-splitters-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Affinda Workspaces API

Workspaces group together related collections, documents, members, and webhook subscriptions. Workspace identifiers scope every document upload, listing, and webhook delivery. Includes per-workspace usage reporting for credits and pages processed.

- **Human URL:** [https://docs.affinda.com/reference/workspaces](https://docs.affinda.com/reference/workspaces)

#### Tags

- Workspaces
- Organization
- Permissions

#### Properties

- [Documentation](https://docs.affinda.com/reference/workspaces)
- [OpenAPI](openapi/affinda-workspaces-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/affinda-workspaces-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/affinda-workspaces-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Affinda Organizations API

Manage the top-level organization account — read and update organization details. Organizations contain users, billing, document types, and workspaces. Per-user limit of 3 API keys.

- **Human URL:** [https://docs.affinda.com/reference](https://docs.affinda.com/reference)

#### Tags

- Organization
- Administration
- Account

#### Properties

- [Documentation](https://docs.affinda.com/reference)
- [OpenAPI](openapi/affinda-organizations-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/affinda-organizations-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/affinda-organizations-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Affinda Invitations API

Create, list, and respond to invitations adding users to the organization. Supports invitation token lookup for join flows and revocation of pending invitations.

- **Human URL:** [https://docs.affinda.com/reference](https://docs.affinda.com/reference)

#### Tags

- Organization
- Members
- Invitations

#### Properties

- [Documentation](https://docs.affinda.com/reference)
- [OpenAPI](openapi/affinda-invitations-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/affinda-invitations-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/affinda-invitations-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Affinda Data Sources API

Manage custom mapping data sources — master-data lists used to match raw extracted values (vendor names, SKUs, categories) to known canonical entities. Upload values via the API and reference the data source from a document type field to enable automatic data matching during parsing.

- **Human URL:** [https://docs.affinda.com/reference](https://docs.affinda.com/reference)

#### Tags

- Data Sources
- Master Data
- Matching

#### Properties

- [Documentation](https://docs.affinda.com/reference)
- [OpenAPI](openapi/affinda-data-sources-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/affinda-data-sources-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/affinda-data-sources-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Affinda Annotations API

Manually create, update, and delete annotations on uploaded documents. Annotations are the field-level extraction objects (value, confidence, bounding box, parent field) and provide the surface for human-in-the-loop validation and review. Supports batch create, update, and delete for high-throughput review workflows.

- **Human URL:** [https://docs.affinda.com/reference/annotations](https://docs.affinda.com/reference/annotations)

#### Tags

- Annotations
- Validation
- Human in the Loop

#### Properties

- [Documentation](https://docs.affinda.com/reference/annotations)
- [OpenAPI](openapi/affinda-annotations-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/affinda-annotations-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/affinda-annotations-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Affinda Validation Results API

Track the status and findings of validation rules attached to parsed documents. Validation results record passes, failures, and remediation context for field-level rules and inform the embeddable validation UI. Supports batch create and delete.

- **Human URL:** [https://docs.affinda.com/reference](https://docs.affinda.com/reference)

#### Tags

- Validation
- Quality
- Human in the Loop

#### Properties

- [Documentation](https://docs.affinda.com/reference)
- [OpenAPI](openapi/affinda-validation-results-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/affinda-validation-results-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/affinda-validation-results-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Affinda Tags API

Tag management for parsed documents. Tags can be arbitrarily attached to documents to support routing, segmentation, search filters, and downstream workflow triggers. Supports batch-add and batch-remove on document collections.

- **Human URL:** [https://docs.affinda.com/reference](https://docs.affinda.com/reference)

#### Tags

- Tags
- Metadata
- Organization

#### Properties

- [Documentation](https://docs.affinda.com/reference)
- [OpenAPI](openapi/affinda-tags-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/affinda-tags-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/affinda-tags-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Affinda Usage API

Retrieve daily credits consumption for the organization across all workspaces and document types. Used for billing reconciliation, budget tracking, and FinOps reporting.

- **Human URL:** [https://docs.affinda.com/reference](https://docs.affinda.com/reference)

#### Tags

- Usage
- Credits
- Reporting
- FinOps

#### Properties

- [Documentation](https://docs.affinda.com/reference)
- [OpenAPI](openapi/affinda-usage-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/affinda-usage-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/affinda-usage-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Affinda Webhooks API

Resthook-style webhook subscriptions for document parsing events. Create a subscription, receive a probe payload, and call the activation endpoint to confirm the receiver. Affinda delivers events such as document parsed, document failed, and validation completed to the registered URL.

- **Human URL:** [https://docs.affinda.com/reference/webhooks](https://docs.affinda.com/reference/webhooks)

#### Tags

- Webhooks
- Events
- Integration

#### Properties

- [Documentation](https://docs.affinda.com/reference/webhooks)
- [OpenAPI](openapi/affinda-webhooks-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/affinda-webhooks-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/affinda-webhooks-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Affinda Search and Match API

Resume search, job description search, and matching across parsed-document indexes. Score candidates against a job description (or vice versa), retrieve match details, configure search and embed parameters, and request job-title and skill suggestions. Includes index management for organizing parsed documents and embeddable UI configuration for resume and JD search components.

- **Human URL:** [https://docs.affinda.com/reference](https://docs.affinda.com/reference)

#### Tags

- Search
- Matching
- Resume Search
- Job Description Search
- Recruitment

#### Properties

- [Documentation](https://docs.affinda.com/reference)
- [OpenAPI](openapi/affinda-search-match-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/affinda-search-match-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/affinda-search-match-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Arazzo Workflows](arazzo/) — [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)
- [Portal](https://www.affinda.com)
- [Documentation](https://docs.affinda.com)
- [Getting Started](https://docs.affinda.com/reference/getting-started)
- [OpenAPI](https://api.affinda.com/static/v3/api_spec.yaml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Agent Skill](https://docs.affinda.com/skill.md)
- [API Reference](https://docs.affinda.com/reference)
- [Pricing](https://www.affinda.com/pricing)
- [Sign Up](https://app.affinda.com/auth/register)
- [Login](https://app.affinda.com/auth/login)
- [Login](https://app.us1.affinda.com/auth/login)
- [Login](https://app.eu1.affinda.com/auth/login)
- [Authentication](https://docs.affinda.com/reference/authentication)
- [Webhooks](https://docs.affinda.com/reference/webhooks)
- [Changelog](https://docs.affinda.com/changelog)
- [Blog](https://www.affinda.com/blog)
- [Academy](https://www.affinda.com/affinda-academy)
- [Support](https://support.affinda.com)
- [Contact Us](https://www.affinda.com/contact)
- [Security](https://www.affinda.com/security)
- [Terms of Service](https://www.affinda.com/legal/terms-of-use)
- [Privacy Policy](https://www.affinda.com/legal/privacy-policy)
- [GitHub Organization](https://github.com/affinda)
- [LinkedIn](https://www.linkedin.com/company/affinda)
- [Twitter](https://twitter.com/affinda_ai)
- [SDK](https://github.com/affinda/affinda-python)
- [SDK](https://github.com/affinda/affinda-typescript)
- [SDK](https://www.npmjs.com/package/@affinda/affinda)
- [SDK](https://pypi.org/project/affinda/)
- [SDK](https://www.nuget.org/packages/Affinda.API)
- [SDK](https://central.sonatype.com/artifact/com.affinda.api/affinda-api-client)
- [Regions](undefined)
- [Compliance](undefined)
- [Plans](plans/affinda-plans-pricing.yml)
- [Rate Limits](rate-limits/affinda-rate-limits.yml)
- [Fin Ops](finops/affinda-finops.yml)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
