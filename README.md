# Citrix NetScaler (citrix-netscaler)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Citrix NetScaler is an application delivery controller (ADC) that provides load balancing, traffic management, application security, and application acceleration capabilities for web applications and services.

**APIs.json:** [https://www.citrix.com/products/citrix-adc/](https://www.citrix.com/products/citrix-adc/)

## Tags

- API Gateway
- Application Delivery Controller
- Application Security
- Load Balancing
- SSL Offloading
- Traffic Management
- Web Application Firewall

## Timestamps

- **Created:** 2024
- **Modified:** 2026-05-19

## APIs

### Citrix ADC (NetScaler) NITRO API

The NITRO API provides programmatic access to configure and monitor NetScaler appliances. It supports REST-based operations for comprehensive management of ADC features including load balancing, content switching, SSL, and more.

- **Human URL:** [https://developer-docs.netscaler.com/en-us/adc-nitro-api/current-release.html](https://developer-docs.netscaler.com/en-us/adc-nitro-api/current-release.html)
- **Base URL:** `https://<netscaler-ip>/nitro/v1`

#### Tags

- Automation
- Configuration
- Monitoring
- REST API

#### Properties

- [Documentation](https://developer-docs.netscaler.com/en-us/adc-nitro-api/current-release.html)
- [OpenAPI](openapi/citrix-netscaler-nitro-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/citrix-netscaler-nitro.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/citrix-netscaler-nitro.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/citrix-netscaler-vserver-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/citrix-netscaler-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [OpenAPI](https://developer-docs.netscaler.com/en-us/adc-nitro-api/current-release/api-reference.html) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Authentication](https://developer-docs.netscaler.com/en-us/adc-nitro-api/current-release/performing-basic-netscaler-operations.html)
- [Getting Started](https://developer-docs.netscaler.com/en-us/adc-nitro-api/current-release/before-you-begin.html)
- [SDK](https://www.citrix.com/downloads/citrix-adc/sdks/)
- [Changelog](https://developer-docs.netscaler.com/en-us/adc-nitro-api/current-release/nitro-changes-across-releases/)

### NetScaler ADM NITRO API

The NetScaler Application Delivery Management (ADM) NITRO API provides programmatic access to manage, monitor, and orchestrate multiple NetScaler instances from a centralized platform, covering analytics, configuration audit, and system management.

- **Human URL:** [https://developer-docs.netscaler.com/en-us/citrix-adm-nitro-api-reference/](https://developer-docs.netscaler.com/en-us/citrix-adm-nitro-api-reference/)
- **Base URL:** `https://<adm-ip>/nitro/v1`

#### Tags

- Analytics
- Management
- Orchestration
- REST API

#### Properties

- [Documentation](https://developer-docs.netscaler.com/en-us/citrix-adm-nitro-api-reference/)
- [Authentication](https://developer-docs.netscaler.com/en-us/citrix-adm-nitro-api-reference/configuration/system/Authentication/Authentication.html)
- [Postman Collection](collections/citrix-netscaler-nitro.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/citrix-netscaler-nitro.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### NetScaler SDX NITRO API

The NetScaler SDX NITRO API provides programmatic access to configure and manage NetScaler SDX appliances via REST interfaces, enabling provisioning and management of multiple virtual NetScaler instances on a single hardware platform.

- **Human URL:** [https://developer-docs.netscaler.com/en-us/adc-sdx-nitro-api-reference/current-release.html](https://developer-docs.netscaler.com/en-us/adc-sdx-nitro-api-reference/current-release.html)
- **Base URL:** `https://<sdx-ip>/nitro/v1`

#### Tags

- Management
- REST API
- SDX
- Virtualization

#### Properties

- [Documentation](https://developer-docs.netscaler.com/en-us/adc-sdx-nitro-api-reference/current-release.html)
- [API Reference](https://developer-docs.netscaler.com/en-us/adc-sdx-nitro-api-reference/adc-sdx-nitro-api-reference.html)
- [Postman Collection](collections/citrix-netscaler-nitro.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/citrix-netscaler-nitro.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### NetScaler Next-Gen API

NetScaler Next-Gen API is a modern declarative RESTful API built on the OpenAPI 3.0 specification that allows developers to programmatically configure NetScaler with an intuitive application-centric interface, abstracting away low-level configuration complexities.

- **Human URL:** [https://developer-docs.netscaler.com/en-us/nextgen-api.html](https://developer-docs.netscaler.com/en-us/nextgen-api.html)
- **Base URL:** `https://<netscaler-ip>/`

#### Tags

- Application-Centric
- Declarative
- OpenAPI
- REST API

#### Properties

- [Documentation](https://developer-docs.netscaler.com/en-us/nextgen-api.html)
- [Getting Started](https://developer-docs.netscaler.com/en-us/nextgen-api/getting-started-guide.html)
- [API Reference](https://developer-docs.netscaler.com/en-us/nextgen-api/apis/)
- [Postman Collection](collections/citrix-netscaler-nitro.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/citrix-netscaler-nitro.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Portal](https://www.netscaler.com/platform/apis)
- [Documentation](https://developer-docs.netscaler.com/)
- [Documentation](https://docs.netscaler.com/)
- [C L I](https://developer-docs.netscaler.com/en-us/adc-command-reference-int/current-release.html)
- [Blog](https://www.netscaler.com/blog/)
- [GitHub Repository](https://github.com/netscaler)
- [GitHub Organization](https://github.com/citrix)
- [Support](https://www.netscaler.com/resources/support)
- [Status Page](https://status.cloud.com/)
- [Sign Up](https://onboarding.cloud.com/)
- [Login](https://citrix.cloud.com/)
- [Privacy Policy](https://www.cloud.com/legal)
- [Terms of Service](https://www.cloud.com/legal)
- [X (Twitter)](https://x.com/NetScaler)
- [LinkedIn](https://www.linkedin.com/company/netscaler)
- [Release Notes](https://docs.netscaler.com/en-us/citrix-adc/current-release/citrix-adc-release-notes.html)
- [Features](undefined)
- [Use Cases](undefined)
- [Integrations](undefined)
- [Integrations](https://www.citrix.com/partners/)

## Maintainers

**Email:** kin@apievangelist.com
**URL:** https://apievangelist.com/
