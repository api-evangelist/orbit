---
name: orbit-create-or-update-member-and-add-identity
description: Create or update a member in a workspace and then add an identity to that member.
api: openapi/orbit-members-api-openapi.yml
operations:
- postByWorkspaceSlugMembers
- postByWorkspaceSlugMembersByMemberSlugIdentities
generated: '2026-10-04'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/orbit-members-api-openapi.yml ; every operationId checked against the contract
---

# orbit-create-or-update-member-and-add-identity

Create or update a member in a workspace and then add an identity to that member.

## Steps

1. 1. Call `postByWorkspaceSlugMembers` with the member data fields required by the API.
2. 2. Call `postByWorkspaceSlugMembersByMemberSlugIdentities` with the member_slug path parameter and the identity fields.

## Rules

- Authentication: include an `Authorization` header using either the `api_key` (apiKey) scheme or a Bearer token (http).
- Pagination: list endpoints support standard pagination parameters (`page`, `per_page`).
