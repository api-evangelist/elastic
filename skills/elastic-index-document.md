---
name: elastic-index-document
description: Create or update a document in an index and retrieve it.
api: openapi/elasticsearch.json
operations:
- index
- get
generated: '2026-10-03'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/elasticsearch.json ; every operationId checked against the contract
---

# elastic-index-document

Create or update a document in an index and retrieve it.

## Steps

1. 1. Use `index` (PUT /{index}/_doc/{id}) with the document fields in the request body.
2. 2. Use `get` (GET /{index}/_doc/{id}) to retrieve the newly indexed document.

## Rules

- Auth: Provide an API key in the `Authorization` header (apiKeyAuth) or use basic or bearer authentication as supported.
- Idempotency: The `index` operation with a specific document ID is idempotent; repeated calls overwrite the same document.
