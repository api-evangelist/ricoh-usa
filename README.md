# Ricoh USA (ricoh-usa)

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

Ricoh USA is the United States operating company of Ricoh Co., Ltd. — a global imaging, printing, document
services, and workplace technology vendor. Beyond its printer / MFP and managed document services portfolio,
Ricoh exposes developer surfaces under three umbrellas: (1) Ricoh Smart Integration, a cloud workflow platform
that connects MFPs to cloud storage and processing services; (2) RICOH360, a developer platform with a Cloud
API for managing 360-degree spatial imagery; and (3) the open RICOH THETA Web / Bluetooth / USB APIs that
control THETA 360 cameras directly. The THETA APIs and SDKs are published openly on GitHub; Ricoh360 Cloud
API access is gated behind application approval; the older Ricoh Smart Integration developer endpoints
(smartintegrationapi.com / api.smartintegrationapi.com) are not currently publicly reachable.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/ricoh-usa/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/ricoh-usa/refs/heads/main/apis.yml)

## Scope

- **Type:** Index

## Tags

- Printing
- Document Management
- Workplace Services
- Imaging
- 360 Cameras
- Workflow Automation

## Timestamps

- **Created:** 2026-05-23
- **Modified:** 2026-05-23

## APIs

### RICOH THETA Web API

HTTP-over-Wi-Fi API for controlling RICOH THETA 360 cameras (Z1, X, A1). Conforms to the Open Spherical
Camera (OSC) API Level 2 specification by Google, with Ricoh vendor extensions. Exposes a small set of
protocol endpoints (/osc/info, /osc/state, /osc/commands/execute, /osc/commands/status) plus a catalog
of 26+ OSC commands such as camera.takePicture, camera.startCapture, camera.listFiles, camera.getOptions,
camera.setOptions, and plugin-control commands. The device acts as an access point or client-mode peer.

- **Human URL:** [https://docs-theta-api.ricoh360.com/web-api/](https://docs-theta-api.ricoh360.com/web-api/)
- **Base URL:** `http://192.168.1.1`

#### Tags

- 360 Cameras
- Imaging
- OSC
- Camera Control

#### Properties

- [Documentation](https://docs-theta-api.ricoh360.com/web-api/)
- [Getting Started](https://ricoh360.notion.site/THETA-API-Guidance-2782875d3632434f9049a641de642142)
- [Source Spec](https://github.com/ricohapi/theta-api-specs/tree/main/theta-web-api-v2.1)
- [OpenAPI](openapi/theta-web-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/theta-web-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/theta-web-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/theta-web-api-device-info-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/theta-web-api-camera-state-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/theta-web-api-command-execute-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/theta-web-api-file-entry-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/ricoh-usa-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Spectral Rules](rules/theta-web-api-rules.yml)
- [Examples](examples/theta-web-api-take-picture-example.json)
- [Examples](examples/theta-web-api-list-files-example.json)
- [Examples](examples/theta-web-api-get-options-example.json)

### RICOH THETA Bluetooth API

GATT-based Bluetooth Low Energy API for controlling RICOH THETA cameras (V, Z1, X, A1). Built on
Bluetooth 4.2 Core Specifications with Ricoh-specific service and characteristic extensions for
shutter control, status reporting, camera information, and Wi-Fi pairing handoff.

- **Human URL:** [https://docs-theta-api.ricoh360.com/bluetooth-api/](https://docs-theta-api.ricoh360.com/bluetooth-api/)

#### Tags

- 360 Cameras
- Bluetooth
- GATT
- Camera Control

#### Properties

- [Documentation](https://docs-theta-api.ricoh360.com/bluetooth-api/)
- [Source Spec](https://github.com/ricohapi/theta-api-specs/tree/main/theta-bluetooth-api)
- [SDK](https://github.com/ricohapi/theta-ble-client)
- [Postman Collection](collections/theta-web-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/theta-web-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### RICOH THETA USB API

MTP (Media Transfer Protocol v1.1) based USB API for controlling RICOH THETA cameras (S and later,
including Z1, X, A1) when tethered over USB. Uses standard MTP operations with Ricoh-proprietary
extensions for live preview, plugin management, and 360 metadata access.

- **Human URL:** [https://docs-theta-api.ricoh360.com/usb-api/](https://docs-theta-api.ricoh360.com/usb-api/)

#### Tags

- 360 Cameras
- USB
- MTP
- Camera Control

#### Properties

- [Documentation](https://docs-theta-api.ricoh360.com/usb-api/)
- [Source Spec](https://github.com/ricohapi/theta-api-specs/tree/main/theta-usb-api)
- [Sample Code](https://github.com/ricohapi/libuvc-theta-sample)
- [Postman Collection](collections/theta-web-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/theta-web-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### RICOH360 Cloud API

Hosted REST API for capture, upload, sharing, and management of 360-degree imagery from RICOH THETA
and partner spherical cameras. Provides serverless image processing, AI-powered editing, virtual tour
creation, archiving, and bulk device administration (firmware updates, configuration). API access
requires application approval through RICOH360 sales / developer contact — no self-service signup.

- **Human URL:** [https://www.ricoh360.com/developer/](https://www.ricoh360.com/developer/)

#### Tags

- 360 Cameras
- Cloud
- Image Processing
- Spatial Data

#### Properties

- [Documentation](https://docs.ricoh360.com/)
- [Portal](https://www.ricoh360.com/developer/)
- [Contact Sales](https://link.ricoh360.com/contact)
- [Postman Collection](collections/theta-web-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/theta-web-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)


#### Tags

- Workflow Automation
- MFP
- Document Management
- Cloud Storage
- OCR

#### Properties

- [Marketing](https://www.ricoh-usa.com/en/services-and-solutions)
- [Contact Sales](https://www.ricoh-usa.com/en/support-and-download/contact-us)
- [Postman Collection](collections/theta-web-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/theta-web-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Website](https://www.ricoh-usa.com/)
- [Parent Website](https://www.ricoh.com/)
- [GitHub Organization](https://github.com/ricohapi)
- [Developer Portal](https://www.ricoh360.com/developer/)
- [Documentation](https://docs.ricoh360.com/)
- [Support](https://www.ricoh-usa.com/en/support-and-download)
- [Contact Sales](https://www.ricoh-usa.com/en/support-and-download/contact-us)
- [LinkedIn](https://www.linkedin.com/company/ricoh-usa-inc-)
- [Careers](https://www.ricoh-usa.com/en/about-us/careers)
- [Case Studies](https://www.ricoh-usa.com/en/insights/case-studies)
- [Vocabulary](vocabulary/ricoh-usa-vocabulary.yml)
- [JSON-LD](json-ld/ricoh-usa-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Plans](plans/ricoh-usa-plans-pricing.yml)
- [Rate Limits](rate-limits/ricoh-usa-rate-limits.yml)
- [Fin Ops](finops/ricoh-usa-finops.yml)
- [Features](undefined)
- [Use Cases](undefined)
- [Integrations](undefined)
- [Git Hub](undefined)
- [SDK](undefined)
- [Tools](undefined)
- [Samples](undefined)
- [Capabilities](undefined)

## Maintainers

**FN:** API Evangelist
**Email:** info@apievangelist.com
