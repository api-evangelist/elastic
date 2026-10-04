---
name: elastic-search-async-flow
description: Run an asynchronous search, poll its status, and retrieve the results.
api: openapi/elasticsearch.json
operations:
- async-search-submit
- async-search-status
- async-search-get
- async-search-delete
generated: '2026-10-03'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/elasticsearch.json ; every operationId checked against the contract
---

# elastic-search-async-flow

Run an asynchronous search, poll its status, and retrieve the results.

## Steps

1. 1. Submit the async search using `async-search-submit` (body: query DSL, optional parameters: `wait_for_completion_timeout`, `keep_on_completion`).
2. 2. Check the search status with `async-search-status` (path parameter: `id`).
3. 3. Retrieve the completed results with `async-search-get` (path parameter: `id`).
4. 4. Optionally delete the async search with `async-search-delete` (path parameter: `id`).

## Rules

- Include an `Authorization` header with the API key, basic token, or bearer token as defined by the provider's auth schemes.
- The async search operations are not rate‑limited; no special handling for exhaustion is required.
- If the async search is not yet complete, `async-search-status` returns a `running` state; poll until `completed` before calling `async-search-get`.
