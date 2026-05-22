# Paragon (paragon)

Paragon is the Integration Infrastructure Platform for B2B SaaS and AI products. The platform combines **Connect Portal** (managed user authentication for 130+ SaaS apps), **Workflows** (event-driven async orchestration), **ActionKit** (Universal API + MCP server giving AI agents synchronous CRUD access to Integration Tools), **Triggers** (event subscriptions), **Managed Sync** (normalized RAG-grade data ingestion with a permissions graph), the **Proxy API** (direct passthrough to third-party APIs on behalf of Connected Users), the **Users API**, and the **Task History API**.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/paragon/refs/heads/main/apis.yml)

## Scope

- **Type:** Contract
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

- **Created:** 2025-06-05
- **Modified:** 2026-05-22

## APIs

### Proxy API

Send requests directly to an integration provider on behalf of Connected Users. Supports any HTTP verb and accepts JSON request bodies.

- **Human URL:** https://docs.useparagon.com/apis/making-api-requests
- **OpenAPI:** [openapi/paragon-proxy-api-openapi.yml](openapi/paragon-proxy-api-openapi.yml)
- **Capabilities:** [capabilities/proxy-proxy.yaml](capabilities/proxy-proxy.yaml), [capabilities/proxy-custom-integrations.yaml](capabilities/proxy-custom-integrations.yaml)
- **Example:** [examples/proxy-request-example.json](examples/proxy-request-example.json)

### Users API

Query and modify the state of Connected Users and their integrations — user info, metadata, integration management, credentials.

- **Human URL:** https://docs.useparagon.com/apis/users
- **OpenAPI:** [openapi/paragon-users-api-openapi.yml](openapi/paragon-users-api-openapi.yml)
- **Schemas:** [json-schema/user.json](json-schema/user.json), [json-schema/integration.json](json-schema/integration.json), [json-schema/credential.json](json-schema/credential.json)
- **Capabilities:** [capabilities/users-users.yaml](capabilities/users-users.yaml), [capabilities/users-integrations.yaml](capabilities/users-integrations.yaml), [capabilities/users-credentials.yaml](capabilities/users-credentials.yaml)
- **Example:** [examples/users-get-user-example.json](examples/users-get-user-example.json)

### Task History API

Query historical workflow executions and step executions. Enterprise plan; rate limited to 1,000 requests per 10 minutes.

- **Human URL:** https://docs.useparagon.com/apis/task-history
- **OpenAPI:** [openapi/paragon-task-history-api-openapi.yml](openapi/paragon-task-history-api-openapi.yml)
- **Schemas:** [json-schema/workflow-execution.json](json-schema/workflow-execution.json), [json-schema/workflow-execution-list.json](json-schema/workflow-execution-list.json)
- **Capability:** [capabilities/task-history-task-history.yaml](capabilities/task-history-task-history.yaml)
- **Example:** [examples/task-history-workflow-executions-example.json](examples/task-history-workflow-executions-example.json)

### ActionKit API

"An API to give your AI agent or app access to Paragon's catalog of pre-built Integration Tools and Triggers." Paired with the Paragon MCP server so agents can call Integration Tools via the Model Context Protocol. 50 req/sec/workspace.

- **Human URL:** https://docs.useparagon.com/actionkit/overview
- **OpenAPI:** [openapi/paragon-actionkit-api-openapi.yml](openapi/paragon-actionkit-api-openapi.yml)
- **Schema:** [json-schema/action.json](json-schema/action.json)
- **Capability:** [capabilities/actionkit-tools.yaml](capabilities/actionkit-tools.yaml)
- **MCP Server:** https://github.com/useparagon/paragon-mcp
- **Examples:** [examples/actionkit-list-actions-example.json](examples/actionkit-list-actions-example.json), [examples/actionkit-run-action-example.json](examples/actionkit-run-action-example.json)

### Triggers API

Beta. Subscribe to events from users' integrations across 130+ SaaS apps using pre-built triggers or custom webhooks.

- **Human URL:** https://docs.useparagon.com/actionkit/triggers/overview
- **OpenAPI:** [openapi/paragon-triggers-api-openapi.yml](openapi/paragon-triggers-api-openapi.yml)
- **Schemas:** [json-schema/trigger.json](json-schema/trigger.json), [json-schema/trigger-subscription.json](json-schema/trigger-subscription.json)
- **Capability:** [capabilities/actionkit-triggers.yaml](capabilities/actionkit-triggers.yaml)
- **Example:** [examples/triggers-subscribe-example.json](examples/triggers-subscribe-example.json)

### Managed Sync API

"Pipelines to sync data from your users' integration sources to your app or RAG pipeline." Covers File Storage, CRM, and Ticketing, with a ReBAC-style permissions graph (check-access, batch-check, list-users, list-objects, expand) for permissions-aware RAG.

- **Human URL:** https://docs.useparagon.com/managed-sync/overview
- **OpenAPI:** [openapi/paragon-managed-sync-api-openapi.yml](openapi/paragon-managed-sync-api-openapi.yml)
- **Schemas:** [json-schema/synced-record.json](json-schema/synced-record.json), [json-schema/sync-status.json](json-schema/sync-status.json), [json-schema/access-check.json](json-schema/access-check.json)
- **Capabilities:** [capabilities/managed-sync-sync.yaml](capabilities/managed-sync-sync.yaml), [capabilities/managed-sync-permissions.yaml](capabilities/managed-sync-permissions.yaml)
- **Examples:** [examples/managed-sync-pull-records-example.json](examples/managed-sync-pull-records-example.json), [examples/permissions-check-access-example.json](examples/permissions-check-access-example.json)

## Plans, Rate Limits, FinOps

- **Plans / Pricing:** [plans/paragon-plans-pricing.yml](plans/paragon-plans-pricing.yml) — Pro / Platform / Enterprise, custom-quoted, scales with Connected Users.
- **Rate Limits:** [rate-limits/paragon-rate-limits.yml](rate-limits/paragon-rate-limits.yml) — Connect 600 req/min, ActionKit 50 req/sec, Task History 1,000/10m; concurrency 5 / 20 / up to 1,000.
- **FinOps (FOCUS):** [finops/paragon-finops.yml](finops/paragon-finops.yml).

## Semantic Layer

- **JSON-LD Context:** [json-ld/paragon-context.jsonld](json-ld/paragon-context.jsonld)
- **Vocabulary:** [vocabulary/paragon-vocabulary.yml](vocabulary/paragon-vocabulary.yml)
- **Spectral Rules:** [rules/paragon-rules.yml](rules/paragon-rules.yml)
- **JSON Structures:** [json-structure/](json-structure/)

## Common Properties

- [GitHub Organization](https://github.com/useparagon)
- [Documentation](https://docs.useparagon.com/overview)
- [Integrations Catalog](https://docs.useparagon.com/resources/integrations) (130+ integrations)
- [MCP Server (paragon-mcp)](https://github.com/useparagon/paragon-mcp)
- [Agent Skills (paragon-ai-skills)](https://github.com/useparagon/paragon-ai-skills)
- [Blog](https://www.useparagon.com/blog)
- [Status](https://status.useparagon.com/)
- [Use Cases](https://www.useparagon.com/use-case/library)
- [SDK (@useparagon/connect)](https://www.npmjs.com/package/@useparagon/connect)
- [Connect Portal](https://docs.useparagon.com/connect-portal/overview)
- [Custom Webhooks](https://docs.useparagon.com/resources/custom-webhooks)
- [RBAC](https://docs.useparagon.com/managing-account/role-based-access-control)
- [Concurrency SLA](https://docs.useparagon.com/billing/concurrency-limits)
- [Security](https://docs.useparagon.com/security/security)
- [Trust Center](https://security.useparagon.com/)
- [GDPR](https://docs.useparagon.com/security/gdpr)
- [HIPAA](https://docs.useparagon.com/security/hipaa)
- [Workflows](https://docs.useparagon.com/workflows/overview)
- [Changelog](https://docs.useparagon.com/changelog/product-updates)
- [Pricing](https://www.useparagon.com/pricing)
- [Customers](https://www.useparagon.com/customers)
- [Sign Up](https://dashboard.useparagon.com/signup) / [Login](https://dashboard.useparagon.com/login)
- AWS On-Prem: [aws-on-prem](https://github.com/useparagon/aws-on-prem), [enterprise-installer](https://github.com/useparagon/enterprise-installer)
- Samples: [paragon-connect-nextjs-example](https://github.com/useparagon/paragon-connect-nextjs-example), [connect-headless-example](https://github.com/useparagon/connect-headless-example), [paragon-rails-example](https://github.com/useparagon/paragon-rails-example), [rag-tutorials](https://github.com/useparagon/rag-tutorials), [actionkit-playground](https://github.com/useparagon/actionkit-playground)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
