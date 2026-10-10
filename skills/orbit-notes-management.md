---
name: orbit-notes-management
description: Create, retrieve, and update a member's notes in an Orbit workspace.
api: openapi/orbit-notes-api-openapi.yml
operations:
- postByWorkspaceSlugMembersByMemberSlugNotes
- getByWorkspaceSlugMembersByMemberSlugNotes
- putByWorkspaceSlugMembersByMemberSlugNotesById
generated: '2026-10-04'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/orbit-notes-api-openapi.yml ; every operationId checked against the contract
---

# orbit-notes-management

Create, retrieve, and update a member's notes in an Orbit workspace.

## Steps

1. 1. `postByWorkspaceSlugMembersByMemberSlugNotes` – provide `workspace_slug`, `member_slug`, and request body fields `content` (string) and optional `type` (string).
2. 2. `getByWorkspaceSlugMembersByMemberSlugNotes` – provide `workspace_slug` and `member_slug` as path parameters; optional query parameters `page` and `per_page` for pagination.
3. 3. `putByWorkspaceSlugMembersByMemberSlugNotesById` – provide `workspace_slug`, `member_slug`, `id` (note ID) and request body fields `content` (string) and optional `type` (string).

## Rules

- Authentication: include an `Authorization` header with either an API key (`api_key`) or a Bearer token (`Bearer <token>`).
- Pagination: `getByWorkspaceSlugMembersByMemberSlugNotes` supports `page` and `per_page` query parameters.
- Idempotency: the `PUT` operation (`putByWorkspaceSlugMembersByMemberSlugNotesById`) is idempotent; repeated calls with the same payload will not create duplicate notes.
