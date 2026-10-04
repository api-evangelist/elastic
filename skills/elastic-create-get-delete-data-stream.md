---
name: elastic-create-get-delete-data-stream
description: Create a data stream, retrieve its details, and then delete it.
api: openapi/elasticsearch.json
operations:
- indices-create-data-stream
- indices-get-data-stream-1
- indices-delete-data-stream
generated: '2026-10-03'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/elasticsearch.json ; every operationId checked against the contract
---

# elastic-create-get-delete-data-stream

Create a data stream, retrieve its details, and then delete it.

## Steps

1. 1. Use `indices-create-data-stream` with the required path parameter `name` and any necessary request body.
2. 2. Use `indices-get-data-stream-1` with the path parameter `name` to retrieve the data stream.
3. 3. Use `indices-delete-data-stream` with the path parameter `name` to delete the data stream.

## Rules

- Auth: Include an `Authorization` header using one of the supported schemes (apiKeyAuth, basicAuth, bearerAuth).
