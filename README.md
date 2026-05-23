# Ricoh USA (ricoh-usa)

Ricoh USA is the United States operating company of Ricoh Co., Ltd. — a global imaging, printing, document services, and workplace technology vendor. Beyond its printer / MFP and managed document services portfolio, Ricoh exposes developer surfaces under three umbrellas: (1) **Ricoh Smart Integration**, a cloud workflow platform that connects MFPs to cloud storage and processing services; (2) **RICOH360**, a developer platform with a Cloud API for managing 360-degree spatial imagery; and (3) the open **RICOH THETA** Web / Bluetooth / USB APIs that control THETA 360 cameras directly. The THETA APIs and SDKs are published openly on GitHub; Ricoh360 Cloud API access is gated behind application approval; the older Ricoh Smart Integration developer endpoints (smartintegrationapi.com / api.smartintegrationapi.com) are not currently publicly reachable.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/ricoh-usa/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

- Printing, Document Management, Workplace Services, Imaging, 360 Cameras, Workflow Automation

## Timestamps

- **Created:** 2026-05-23
- **Modified:** 2026-05-23

## APIs

### RICOH THETA Web API

HTTP-over-Wi-Fi API for controlling RICOH THETA 360 cameras (Z1, X, A1). Conforms to the Open Spherical Camera (OSC) API Level 2 specification by Google, with Ricoh vendor extensions. Exposes a small set of protocol endpoints (`/osc/info`, `/osc/state`, `/osc/commands/execute`, `/osc/commands/status`) plus a catalog of 26+ OSC commands such as `camera.takePicture`, `camera.startCapture`, `camera.listFiles`, `camera.getOptions`, `camera.setOptions`, and plugin-control commands.

**Human URL:** [https://docs-theta-api.ricoh360.com/web-api/](https://docs-theta-api.ricoh360.com/web-api/)

**Base URL:** `http://192.168.1.1` (camera in access-point mode)

#### Properties

- [Documentation](https://docs-theta-api.ricoh360.com/web-api/)
- [Getting Started](https://ricoh360.notion.site/THETA-API-Guidance-2782875d3632434f9049a641de642142)
- [Source Spec (GitHub)](https://github.com/ricohapi/theta-api-specs/tree/main/theta-web-api-v2.1)
- [OpenAPI](openapi/theta-web-api-openapi.yml)
- [Spectral Rules](rules/theta-web-api-rules.yml)
- [Capability — Camera Control](capabilities/theta-camera-control.yaml)
- [Capability — Media Management](capabilities/theta-media-management.yaml)

### RICOH THETA Bluetooth API

GATT-based Bluetooth Low Energy API for controlling RICOH THETA cameras (V, Z1, X, A1). Built on Bluetooth 4.2 Core Specifications with Ricoh-specific service and characteristic extensions for shutter control, status reporting, camera information, and Wi-Fi pairing handoff.

**Human URL:** [https://docs-theta-api.ricoh360.com/bluetooth-api/](https://docs-theta-api.ricoh360.com/bluetooth-api/)

- [Documentation](https://docs-theta-api.ricoh360.com/bluetooth-api/)
- [SDK — theta-ble-client](https://github.com/ricohapi/theta-ble-client)

### RICOH THETA USB API

MTP (Media Transfer Protocol v1.1) based USB API for controlling RICOH THETA cameras tethered over USB. Uses standard MTP operations with Ricoh-proprietary extensions for live preview, plugin management, and 360 metadata access.

**Human URL:** [https://docs-theta-api.ricoh360.com/usb-api/](https://docs-theta-api.ricoh360.com/usb-api/)

- [Documentation](https://docs-theta-api.ricoh360.com/usb-api/)
- [Sample Code — libuvc-theta-sample](https://github.com/ricohapi/libuvc-theta-sample)

### RICOH360 Cloud API

Hosted REST API for capture, upload, sharing, and management of 360-degree imagery from RICOH THETA and partner spherical cameras. Provides serverless image processing, AI-powered editing, virtual tour creation, archiving, and bulk device administration. API access requires application approval — no self-service signup.

**Human URL:** [https://www.ricoh360.com/developer/](https://www.ricoh360.com/developer/)

- [Documentation](https://docs.ricoh360.com/)
- [Developer Portal](https://www.ricoh360.com/developer/)
- [Contact Sales](https://link.ricoh360.com/contact)

### Ricoh Smart Integration

Cloud workflow platform that connects Ricoh multifunction printers and Smart Operation Panel devices to cloud storage (Box, Dropbox, Google Drive, OneDrive, SharePoint), document conversion (OCR / PDF), and Microsoft 365 / email distribution workflows. Previously exposed a documented developer API surface at `smartintegrationapi.com`; those endpoints currently refuse public connections, so partner / SI integrations route through Ricoh USA professional services.

**Human URL:** [https://www.ricoh-usa.com/en/services-and-solutions](https://www.ricoh-usa.com/en/services-and-solutions)

- [Contact Sales](https://www.ricoh-usa.com/en/support-and-download/contact-us)

## Common Properties

- [Website](https://www.ricoh-usa.com/)
- [Parent Website](https://www.ricoh.com/)
- [GitHub Organization (ricohapi)](https://github.com/ricohapi)
- [Developer Portal](https://www.ricoh360.com/developer/)
- [Documentation](https://docs.ricoh360.com/)
- [Support](https://www.ricoh-usa.com/en/support-and-download)
- [Contact Sales](https://www.ricoh-usa.com/en/support-and-download/contact-us)
- [LinkedIn](https://www.linkedin.com/company/ricoh-usa-inc-)
- [Case Studies](https://www.ricoh-usa.com/en/insights/case-studies)

## Features

| Name | Description |
|------|-------------|
| 360-Degree Camera Control | Open OSC, Bluetooth, and USB APIs for controlling THETA spherical cameras programmatically |
| Cloud Image Processing | RICOH360 Cloud API performs AI-assisted 360 image conversion, stitching, blur, and tour creation |
| MFP Workflow Integration | Ricoh Smart Integration connects multifunction printers to cloud storage and document workflows |
| Multi-Language SDKs | THETA Client SDKs cover Android (Kotlin), iOS (Swift), React Native, and Flutter |
| Plugin Architecture | RICOH THETA plug-in SDK enables custom Android-based applications running on the camera |
| Spherical Metadata | IMU / GNSS sensor metadata embedded in JPG and MP4 outputs for spatial reconstruction |
| Bulk Device Management | RICOH360 Cloud API supports firmware updates and configuration of fleets of THETA cameras |
| Live Preview Streaming | Web API `getLivePreview` and USB UVC paths expose real-time spherical preview frames |

## Use Cases

| Name | Description |
|------|-------------|
| Virtual Tours | Capture and publish 360-degree walkthroughs for real estate, construction, and retail |
| Construction Progress Documentation | Periodic 360 captures uploaded to RICOH360 Cloud for site audit and dispute resolution |
| Insurance Inspection | Field adjusters capture spherical scene evidence and sync to claim systems |
| Live Event Streaming | THETA plug-ins (WebRTC, Live Streaming) for 360 broadcasts |
| Scan-to-Cloud Workflows | Smart Integration sends MFP scans directly to Box, Google Drive, OneDrive, or SharePoint |
| Mobile Capture Apps | React Native / Flutter THETA Client apps for field-team capture pipelines |
| Asset Management | Catalog and search large libraries of 360 images via RICOH360 Cloud |
| Process Automation | Ricoh USA professional services build OCR / approval workflows around Smart Integration |

## Integrations

| Name | Description |
|------|-------------|
| Box | Smart Integration supports scan-to-Box workflows |
| Dropbox | Scan-to-cloud target via Smart Integration |
| Google Drive | Scan-to-cloud target via Smart Integration |
| Microsoft OneDrive | Scan-to-cloud target via Smart Integration |
| Microsoft SharePoint | Scan-to-cloud target via Smart Integration |
| Microsoft 365 / Outlook | Email distribution and routing from MFP scans |
| Salesforce | RICOH360 Cloud customer integrations for service / inspection workflows |

## GitHub Organization

[**ricohapi**](https://github.com/ricohapi) — 51 repositories total. Notable active repos:

- [theta-api-specs](https://github.com/ricohapi/theta-api-specs) — canonical THETA API specifications (Web, Bluetooth, USB)
- [theta-client](https://github.com/ricohapi/theta-client) — Kotlin Multiplatform SDK (Android, iOS, React Native, Flutter)
- [theta-ble-client](https://github.com/ricohapi/theta-ble-client) — Bluetooth SDK
- [theta-plugin-sdk](https://github.com/ricohapi/theta-plugin-sdk) — Android-based plug-in SDK for THETA cameras
- [theta-plugin-library](https://github.com/ricohapi/theta-plugin-library) — shared library for THETA plug-ins
- [fake-theta](https://github.com/ricohapi/fake-theta) — THETA API simulator for CI and development
- [awesome-theta](https://github.com/ricohapi/awesome-theta) — curated community list
- [libuvc-theta](https://github.com/ricohapi/libuvc-theta) / [libuvc-theta-sample](https://github.com/ricohapi/libuvc-theta-sample) — USB UVC live-preview support

A large historical set of `ricoh-cloud-*` and `media-storage-*` / `auth-*` SDKs sits archived in the same org (2023), reflecting an earlier generation of the Ricoh Cloud API that has since been superseded by RICOH360.

## Artifacts

Machine-readable API specifications organized by format.

### OpenAPI

- [RICOH THETA Web API](openapi/theta-web-api-openapi.yml)

### JSON Schema

- [Camera Info](json-schema/theta-web-api-device-info-schema.json)
- [Camera State](json-schema/theta-web-api-camera-state-schema.json)
- [Command Execute Envelope](json-schema/theta-web-api-command-execute-schema.json)
- [File Entry](json-schema/theta-web-api-file-entry-schema.json)

### JSON Structure

- [Camera State](json-structure/theta-web-api-camera-state-structure.json)
- [File Entry](json-structure/theta-web-api-file-entry-structure.json)
- [Command Execute Envelope](json-structure/theta-web-api-command-execute-structure.json)

### JSON-LD

- [Ricoh USA Context](json-ld/ricoh-usa-context.jsonld)

### Examples

- [Take Picture](examples/theta-web-api-take-picture-example.json)
- [List Files](examples/theta-web-api-list-files-example.json)
- [Get Options](examples/theta-web-api-get-options-example.json)

## Capabilities

Naftiko capabilities organized as shared per-API definitions composed into customer-facing workflows.

### Shared Per-API Definitions

- [RICOH THETA Web API](capabilities/shared/theta-web-api.yaml) — 18 capabilities covering device info, state, commands, media, options, plug-ins, and network
- [RICOH THETA Bluetooth API](capabilities/shared/theta-bluetooth-api.yaml) — 6 capabilities for GATT discover / shutter / Wi-Fi handoff
- [RICOH THETA USB API](capabilities/shared/theta-usb-api.yaml) — 7 capabilities for MTP / UVC operations
- [RICOH360 Cloud API](capabilities/shared/ricoh360-cloud-api.yaml) — 10 capabilities for upload, processing, tours, fleet management

### Workflow Capabilities

| Workflow | APIs Combined | Persona |
|----------|---------------|---------|
| [THETA Camera Control](capabilities/theta-camera-control.yaml) | RICOH THETA Web API | App Developer |
| [THETA Media Management](capabilities/theta-media-management.yaml) | RICOH THETA Web API | App Developer |

## Vocabulary

- [Ricoh USA Vocabulary](vocabulary/ricoh-usa-vocabulary.yml) — Unified taxonomy across 5 APIs, 10 resources, capability domains (Camera Control, Media Management, Cloud Imagery, Virtual Tour, Fleet Administration, Document Workflow), and 4 personas

## Rules

- [THETA Web API Spectral Rules](rules/theta-web-api-rules.yml) — Spectral rules enforcing OSC `/osc/` path convention, POST-only command envelopes, Title Case summaries, camelCase operationIds, and standard description / response requirements

## Commercial

- [Plans / Pricing](plans/ricoh-usa-plans-pricing.yml) — Free open device APIs (bundled with THETA hardware), enterprise-only RICOH360 Cloud and Smart Integration (contact sales)
- [Rate Limits](rate-limits/ricoh-usa-rate-limits.yml) — Exclusive-use serialization on THETA (cameraInExclusiveUse error), contract-defined cloud quotas
- [FinOps Mapping](finops/ricoh-usa-finops.yml) — Hardware CapEx for THETA, OpEx contracts for RICOH360 Cloud and Smart Integration

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
