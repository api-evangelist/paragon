# Paragon (paragon)

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

Paragon is the Integration Infrastructure Platform for B2B SaaS and AI products. The platform combines Connect Portal (managed user authentication for 130+ SaaS apps), Workflows (event-driven async orchestration), ActionKit (Universal API + MCP server giving AI agents synchronous CRUD access to Integration Tools), Triggers (event subscriptions), Managed Sync (normalized RAG-grade data ingestion with a permissions graph), the Proxy API (direct passthrough to third-party APIs on behalf of Connected Users), the Users API, and the Task History API.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/paragon/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/paragon/refs/heads/main/apis.yml)

## Scope

- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- Embedded Integrations
- Integration Infrastructure
- iPaaS
- AI Agents
- MCP
- Integrations

## Timestamps

- **Created:** 2025-06-05T00:00:00.000Z
- **Modified:** 2026-05-22

## APIs

### Proxy API

Send requests directly to an integration provider, on behalf of Connected Users. The Proxy API allows you to access any third-party provider's API methods via Paragon's managed credential handling. Supports any HTTP verb and accepts JSON request bodies. Along with Workflows, the Proxy API is one of two primary ways to build integrations with Paragon.

- **Human URL:** [https://docs.useparagon.com/apis/making-api-requests](https://docs.useparagon.com/apis/making-api-requests)

#### Tags

- Embedded Integrations
- Proxy
- Integrations

#### Properties

- [Documentation](https://docs.useparagon.com/apis/making-api-requests)
- [OpenAPI](openapi/paragon-proxy-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/paragon-proxy-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/paragon-proxy-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON-LD](json-ld/paragon-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Example](examples/proxy-request-example.json)

### Users API

The Users API allows you to query and modify the state of your Connected Users and their integrations. Endpoints cover retrieving user info, setting metadata, listing and disconnecting integrations, and managing Connect credentials. SDK functions like paragon.authenticate(), paragon.setMetadata(), and paragon.uninstallIntegration() map to these endpoints.

- **Human URL:** [https://docs.useparagon.com/apis/users](https://docs.useparagon.com/apis/users)

#### Tags

- Embedded Integrations
- Users
- Integrations

#### Properties

- [Documentation](https://docs.useparagon.com/apis/users)
- [OpenAPI](openapi/paragon-users-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/paragon-users-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/paragon-users-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/user.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/integration.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/credential.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/paragon-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Example](examples/users-get-user-example.json)

### Task History API

The Task History API allows you to query your users' usage of integration workflows and access data from historical workflow executions. Includes endpoints to list and inspect workflow executions, drill into step executions, and replay failed runs. Available on Enterprise plans; rate limited to 1,000 requests per 10 minutes.

- **Human URL:** [https://docs.useparagon.com/apis/task-history](https://docs.useparagon.com/apis/task-history)

#### Tags

- Embedded Integrations
- Task History
- Workflows
- Integrations

#### Properties

- [Documentation](https://docs.useparagon.com/apis/task-history)
- [OpenAPI](openapi/paragon-task-history-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/paragon-task-history-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/paragon-task-history-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/workflow-execution.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/workflow-execution-list.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/paragon-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Example](examples/task-history-workflow-executions-example.json)

### ActionKit API

"ActionKit is an API to give your AI agent or app access to Paragon's catalog of pre-built Integration Tools and Triggers." Exposes a Universal API for listing and executing synchronous CRUD actions across 130+ SaaS integrations, and is paired with the Paragon MCP server (github.com/useparagon/paragon-mcp) so agents can call these tools via the Model Context Protocol. Rate limited to 50 requests per second per workspace.

- **Human URL:** [https://docs.useparagon.com/actionkit/overview](https://docs.useparagon.com/actionkit/overview)

#### Tags

- ActionKit
- AI Agents
- MCP
- Tools
- Integrations

#### Properties

- [Documentation](https://docs.useparagon.com/actionkit/overview)
- [OpenAPI](openapi/paragon-actionkit-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/paragon-actionkit-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/paragon-actionkit-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/action.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/paragon-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [M C P Server](https://github.com/useparagon/paragon-mcp)
- [Example](examples/actionkit-list-actions-example.json)
- [Example](examples/actionkit-run-action-example.json)

### Triggers API

The Triggers API (Beta) lets you "subscribe to events from your users' integrations, using our catalog of pre-built triggers or Custom Webhooks." Exposes discovery, subscription, update, and unsubscribe operations for events such as `SLACK_MESSAGE_RECEIVED` or `GOOGLE_CALENDAR_NEW_EVENT` across 130+ integrations. Authenticates with the Paragon User Token JWT.

- **Human URL:** [https://docs.useparagon.com/actionkit/triggers/overview](https://docs.useparagon.com/actionkit/triggers/overview)

#### Tags

- ActionKit
- Triggers
- Webhooks
- AI Agents
- Integrations

#### Properties

- [Documentation](https://docs.useparagon.com/actionkit/triggers/overview)
- [OpenAPI](openapi/paragon-triggers-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/paragon-triggers-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/paragon-triggers-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/trigger.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/trigger-subscription.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/paragon-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Example](examples/triggers-subscribe-example.json)

### Managed Sync API

"Managed Sync provides pipelines to sync data from your users' integration sources to your app or RAG pipeline." Covers File Storage (Google Drive, Box, OneDrive, S3, Dropbox, SharePoint), CRM, and Ticketing sources, with normalized schemas and a ReBAC-style permissions graph (check-access, batch-check, list-users, list-objects, expand) so applications can enforce source-system permissions when retrieving content for retrieval-augmented generation.

- **Human URL:** [https://docs.useparagon.com/managed-sync/overview](https://docs.useparagon.com/managed-sync/overview)

#### Tags

- Managed Sync
- RAG
- Data Ingestion
- Integrations

#### Properties

- [Documentation](https://docs.useparagon.com/managed-sync/overview)
- [OpenAPI](openapi/paragon-managed-sync-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/paragon-managed-sync-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/paragon-managed-sync-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/synced-record.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/sync-status.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/access-check.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/paragon-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Example](examples/managed-sync-pull-records-example.json)
- [Example](examples/permissions-check-access-example.json)

## Common Properties

- [Arazzo Workflows](arazzo/) — [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)
- [LinkedIn](https://www.linkedin.com/company/paragon)
- [GitHub Organization](https://github.com/useparagon)
- [Integrations](https://www.useparagon.com/integrations)
- [Documentation](https://docs.useparagon.com/overview)
- [Blog](https://www.useparagon.com/blog)
- [Status Page](https://status.useparagon.com/)
- [Use Cases](https://www.useparagon.com/use-case/library)
- [S D Ks](https://docs.useparagon.com/getting-started/installing-the-connect-sdk)
- [S D Ks](https://www.npmjs.com/package/@useparagon/connect)
- [Authentication](https://docs.useparagon.com/connect-portal/overview)
- [Webhooks](https://docs.useparagon.com/resources/custom-webhooks)
- [R B A C](https://docs.useparagon.com/managing-account/role-based-access-control)
- [Service Level Agreement](https://docs.useparagon.com/billing/concurrency-limits)
- [Rate Limits](rate-limits/paragon-rate-limits.yml)
- [Plans](plans/paragon-plans-pricing.yml)
- [Fin Ops](finops/paragon-finops.yml)
- [Security](https://docs.useparagon.com/security/security)
- [Trust](https://security.useparagon.com/)
- [G D P R](https://docs.useparagon.com/security/gdpr)
- [H I P A A](https://docs.useparagon.com/security/hipaa)
- [Support](https://docs.useparagon.com/support/contacting-support)
- [Workflows](https://docs.useparagon.com/workflows/overview)
- [Changelog](https://docs.useparagon.com/changelog/product-updates)
- [Sign Up](https://dashboard.useparagon.com/signup)
- [Login](https://dashboard.useparagon.com/login)
- [Terms of Service](https://www.useparagon.com/terms-of-service)
- [Customers](https://www.useparagon.com/customers)
- [Pricing](https://www.useparagon.com/pricing)
- [M C P Server](https://github.com/useparagon/paragon-mcp)
- [Agent Skill](https://github.com/useparagon/paragon-ai-skills)
- [Sample Code](https://github.com/useparagon/paragon-connect-nextjs-example)
- [Sample Code](https://github.com/useparagon/connect-headless-example)
- [Sample Code](https://github.com/useparagon/paragon-rails-example)
- [Sample Code](https://github.com/useparagon/rag-tutorials)
- [Sample Code](https://github.com/useparagon/actionkit-playground)
- [Deployment](https://github.com/useparagon/aws-on-prem)
- [Deployment](https://github.com/useparagon/enterprise-installer)
- [Vocabulary](vocabulary/paragon-vocabulary.yml)
- [Spectral Ruleset](rules/paragon-rules.yml)
- [JSON Structure](json-structure/paragon-action-structure.json)
- [JSON Structure](json-structure/paragon-synced-record-structure.json)
- [JSON Structure](json-structure/paragon-trigger-subscription-structure.json)
- [Features](https://www.useparagon.com/pricing)
- [Use Cases](https://www.useparagon.com/use-case/library)
- [Integrations](https://docs.useparagon.com/resources/integrations)
- [L L Ms Txt](https://docs.useparagon.com/llms.txt)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
