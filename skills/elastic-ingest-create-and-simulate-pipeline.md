---
name: elastic-ingest-create-and-simulate-pipeline
description: Create or update an ingest pipeline and then simulate it with sample documents.
api: openapi/elasticsearch.json
operations:
- ingest-put-pipeline
- ingest-simulate-1
generated: '2026-10-03'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/elasticsearch.json ; every operationId checked against the contract
---

# elastic-ingest-create-and-simulate-pipeline

Create or update an ingest pipeline and then simulate it with sample documents.

## Steps

1. 1. Use `ingest-put-pipeline` with path parameter `id` and request body defining the pipeline definition.
2. 2. Use `ingest-simulate-1` with request body containing the documents to be processed by the pipeline.

## Rules

- Auth: include an `Authorization` header with an API key, Basic credentials, or Bearer token as defined by the provider's auth schemes.
- Idempotency: `ingest-put-pipeline` is idempotent – sending the same pipeline definition for the same `id` overwrites the existing pipeline.
- Errors: on failure the API returns standard HTTP error codes (e.g., 400 for bad request, 404 for missing pipeline).
