---
name: elastic-indices-create-and-alias
description: Create a new index and assign an alias to it.
api: openapi/elasticsearch.json
operations:
- indices-create
- indices-put-alias
generated: '2026-10-03'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/elasticsearch.json ; every operationId checked against the contract
---

# elastic-indices-create-and-alias

Create a new index and assign an alias to it.

## Steps

1. 1. Call `indices-create` with the required path parameter `{index}` and optional body fields for index settings and mappings.
2. 2. Call `indices-put-alias` with the path parameters `{index}` and `{name}` to create or update the alias for the newly created index.

## Rules

- Auth header: use one of the supported schemes (apiKeyAuth via `Authorization` header, basicAuth, or bearerAuth).
- Idempotency: `indices-create` is not idempotent if the index already exists; `indices-put-alias` is idempotent for the same alias name.
