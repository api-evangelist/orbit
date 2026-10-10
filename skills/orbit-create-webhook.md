---
name: orbit-create-webhook
description: Create a new webhook in a workspace and retrieve its details.
api: openapi/orbit-webhooks-api-openapi.yml
operations:
- postByWorkspaceSlugWebhooks
- getByWorkspaceSlugWebhooksById
generated: '2026-10-04'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/orbit-webhooks-api-openapi.yml ; every operationId checked against the contract
---

# orbit-create-webhook

Create a new webhook in a workspace and retrieve its details.

## Steps

1. 1. Use `postByWorkspaceSlugWebhooks` with body fields `url`, `events`, and optional `active`.
2. 2. Use `getByWorkspaceSlugWebhooksById` with path parameter `id` returned from the create call.

## Rules

- Auth: Include an `Authorization` header with either an API key (`api_key`) or a Bearer token (`bearer`).
- Idempotency: The POST operation is not idempotent; repeat calls will create duplicate webhooks.
