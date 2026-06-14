# Elastic GraphQL Schema

## Overview

This conceptual GraphQL schema covers the Elastic platform — Elasticsearch, Kibana, APM, Machine Learning, Security, and Fleet. It maps the REST API surface described at [https://www.elastic.co/docs/api/doc/elasticsearch](https://www.elastic.co/docs/api/doc/elasticsearch) into a typed GraphQL layer.

The schema is conceptual and intended for design, documentation, and tooling purposes. It is not an officially published GraphQL endpoint from Elastic.

**Provider:** Elastic
**Source:** [https://www.elastic.co/docs/api](https://www.elastic.co/docs/api)
**GitHub:** [https://github.com/elastic](https://github.com/elastic)
**Schema file:** [elastic-schema.graphql](elastic-schema.graphql)

---

## Domain Areas

### Index and Data Management

Types covering Elasticsearch indices, mappings, settings, shards, templates, data streams, component templates, and aliases. These form the structural foundation for storing and retrieving documents.

- `Index`, `IndexMapping`, `IndexSettings`, `IndexStats`, `IndexShard`
- `IndexTemplate`, `ComponentTemplate`, `DataStream`, `Alias`

### Documents and Ingest

Types for individual documents, ingest pipelines, and processors. Covers the lifecycle from raw data arrival through pipeline transformation to indexing.

- `Document`, `Pipeline`, `PipelineProcessor`, `Ingest`

### Search and Query DSL

Types representing the full Elasticsearch query DSL — bool queries, match/term/range/wildcard/fuzzy/geo/nested/percolate queries — plus result wrappers, hits, and aggregations.

- `SearchRequest`, `SearchResult`, `SearchHit`
- `BoolQuery`, `MatchQuery`, `TermQuery`, `RangeQuery`, `WildcardQuery`, `FuzzyQuery`, `GeoQuery`, `NestedQuery`, `PercolateQuery`
- `Aggregation`, `Bucket`, `Metric`

### Cluster and Node Administration

Types for cluster health, cluster state, nodes, and per-node statistics. Used for operational visibility and capacity management.

- `Cluster`, `ClusterHealth`, `ClusterState`, `Node`, `NodeStats`

### Snapshots and Repositories

Types for snapshot lifecycle management, repository configuration, and restore operations.

- `Snapshot`, `Repository`

### Tasks

Type for the Task API, covering long-running async operations.

- `Task`

### Index Lifecycle Management (ILM)

Types for ILM policies, phases, and actions that automate data tier transitions and retention.

- `Lifecycle`, `ILMPolicy`, `ILMPhase`, `ILMAction`

### Rollup and Transforms

Types for rollup jobs that summarize historical data and transform jobs that continuously pivot data into destination indices.

- `Rollup`, `RollupJob`, `Transform`, `TransformProgress`

### Machine Learning

Types for ML jobs, datafeeds, forecasts, trained models, and anomaly records.

- `MlJob`, `MlDatafeed`, `Forecast`, `TrainedModel`, `Anomaly`

### Watcher and Alerting

Types for Watcher watches, execution history, and alert records.

- `WatcherWatch`, `WatchExecution`, `Alert`

### Cross-Cluster Replication (CCR)

Types for CCR follower indices and replication info.

- `CCR`, `CCRInfo`

### Enrich

Types for enrich policies and their execution state.

- `Enrich`, `EnrichPolicy`

### Fleet and APM

Types for Fleet agents and APM services, traces, logs, and metrics.

- `Fleet`, `FleetAgent`, `APMService`, `APMTrace`, `LogEntry`, `MetricDocument`

### Security

Types for users, roles, and API keys managed by Elasticsearch security.

- `SecurityUser`, `SecurityRole`, `ApiKey`

---

## Type Count

This schema defines **72 named types** (object types, input types, enums, and scalars).

---

## Usage Notes

- All `id` fields correspond to the natural identifiers used by the Elasticsearch REST API (index name, document `_id`, job id, etc.).
- Timestamps are represented as the `DateTime` scalar (ISO 8601).
- JSON blobs (mappings source, pipeline definitions) are represented as the `JSON` scalar.
- Pagination uses `offset` and `limit` on list fields; a future extension could adopt Relay-style cursor pagination.
- Mutations map to REST write operations (PUT/POST/DELETE). Query fields map to GET operations.
