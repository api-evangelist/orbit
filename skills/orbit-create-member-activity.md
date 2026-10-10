---
name: orbit-create-member-activity
description: Create a new custom or content activity for a specific member in a workspace.
api: openapi/orbit-activities-api-openapi.yml
operations:
- postByWorkspaceSlugMembersByMemberSlugActivities
- getByWorkspaceSlugMembersByMemberSlugActivities
generated: '2026-10-04'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/orbit-activities-api-openapi.yml ; every operationId checked against the contract
---

# orbit-create-member-activity

Create a new custom or content activity for a specific member in a workspace.

## Steps

1. 1. Use `postByWorkspaceSlugMembersByMemberSlugActivities` with required body fields (e.g., `type`, `title`, `description`, `member_slug`).
2. 2. Optionally verify creation with `getByWorkspaceSlugMembersByMemberSlugActivities` using the same `workspace_slug` and `member_slug`.

## Rules

- Auth: Include either an `api_key` query parameter or a `Authorization: Bearer <token>` header.
- Rate limit: No rate limit is defined; no special handling on exhaustion.
