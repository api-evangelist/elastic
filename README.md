# Elastic (elastic)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Elastic is a software company that builds search-powered solutions for observability, security, and search use cases. The Elastic Stack (Elasticsearch, Kibana, and related tools) lets organizations ingest, search, analyze, and visualize structured and unstructured data in real time. Elastic Cloud delivers managed Elasticsearch and Kibana deployments with REST APIs for both data operations and deployment management.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/elastic/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/elastic/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Producer
- **Access:** 3rd-Party

## Tags

- Search
- Analytics
- Observability
- Security
- Visualization
- Cloud

## Timestamps

- **Created:** 2025-01-08
- **Modified:** 2026-05-19

## APIs

### Elasticsearch REST API

The Elasticsearch REST API powers indexing, search, and cluster administration for the Elasticsearch search and analytics engine. It exposes operations for indexing documents, running queries, managing indices and mappings, snapshots, security roles and API keys, and cluster health.

- **Human URL:** [https://www.elastic.co/docs/api/doc/elasticsearch](https://www.elastic.co/docs/api/doc/elasticsearch)
- **Base URL:** `https://api.elastic-cloud.com`

#### Tags

- Search
- Analytics
- Indexing
- Documents
- Cluster

#### Properties

- [Documentation](https://www.elastic.co/docs/api/doc/elasticsearch)
- [OpenAPI](openapi/elastic-elasticsearch-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/elastic-elasticsearch.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/elastic-elasticsearch.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Kibana API

The Kibana REST API manages Kibana resources including saved objects, data views, Spaces, connectors, and alerting rules. Calls are stateless and use the same authentication mechanisms as Elasticsearch.

- **Human URL:** [https://www.elastic.co/docs/api/doc/kibana](https://www.elastic.co/docs/api/doc/kibana)

#### Tags

- Visualization
- Dashboards
- SavedObjects
- DataViews

#### Properties

- [Documentation](https://www.elastic.co/docs/api/doc/kibana)
- [OpenAPI](openapi/elastic-kibana-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/elastic-kibana.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/elastic-kibana.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Elastic Cloud API

The Elastic Cloud API manages hosted Elasticsearch and Kibana deployments. It supports creating, updating, resizing, snapshotting, and deleting deployments, plus traffic filter and account-level operations.

- **Human URL:** [https://www.elastic.co/docs/api/doc/cloud](https://www.elastic.co/docs/api/doc/cloud)
- **Base URL:** `https://api.elastic-cloud.com`

#### Tags

- Cloud
- Deployments
- Provisioning
- TrafficFilters

#### Properties

- [Documentation](https://www.elastic.co/docs/api/doc/cloud)
- [OpenAPI](openapi/elastic-cloud-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/elastic-cloud.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/elastic-cloud.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/elastic-co)
- [Website](https://www.elastic.co)
- [Documentation](https://www.elastic.co/guide/index.html)
- [Git Hub](https://github.com/elastic)
- [Console](https://cloud.elastic.co)
- [Pricing](https://www.elastic.co/pricing)
- [License](https://www.elastic.co/licensing/elastic-license)
- [Features](undefined)
- [Integrations](https://www.elastic.co/integrations)
- [L L Ms Txt](https://api.elastic-cloud.com/llms.txt)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
