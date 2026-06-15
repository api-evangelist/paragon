# Paragon (paragon)

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
