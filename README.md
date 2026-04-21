# Backblaze (backblaze)
Backblaze is a cloud storage and data backup provider offering B2 Cloud Storage - a low-cost, S3-compatible object storage service. Backblaze provides both a native B2 API and an S3-compatible API, enabling developers to build applications that store unlimited data at a fraction of major cloud provider costs. Features include file versioning, lifecycle rules, event notifications, object lock, cross-region replication, and a Cloudflare bandwidth alliance for zero-egress CDN delivery.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/backblaze/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags:

 - Cloud Storage, Object Storage, Storage, Backup

## Timestamps

- **Created:** 2025-03-01
- **Modified:** 2026-04-19

## APIs

### Backblaze B2 Cloud Storage API
The Backblaze B2 Native API provides programmatic access to all B2 Cloud Storage functions including account authorization, bucket management, file upload and download, large file multi-part uploads, application key management, lifecycle rules, replication, and event notifications. Uses HTTP Basic authentication to obtain authorization tokens for subsequent API calls. API v4 is the current stable version.

**Human URL:** [https://www.backblaze.com/b2/cloud-storage.html](https://www.backblaze.com/b2/cloud-storage.html)

#### Tags:

 - Cloud Storage, Object Storage, Storage

#### Properties

- [Documentation](https://www.backblaze.com/apidocs/introduction-to-the-b2-native-api)
- [GettingStarted](https://www.backblaze.com/docs/cloud-storage-native-api)
- [OpenAPI](openapi/backblaze-b2-native-api.yaml)

### Backblaze S3-Compatible API
The Backblaze S3-Compatible API allows existing applications built for Amazon S3 to work with Backblaze B2 Cloud Storage with minimal code changes. Supports S3 authentication (AWS Signature V4) and S3 API operations for bucket and object management. Endpoint URLs follow the pattern s3.<region>.backblazeb2.com.

**Human URL:** [https://www.backblaze.com/apidocs/introduction-to-the-s3-compatible-api](https://www.backblaze.com/apidocs/introduction-to-the-s3-compatible-api)

#### Tags:

 - Cloud Storage, Object Storage, S3 Compatible

#### Properties

- [Documentation](https://www.backblaze.com/apidocs/introduction-to-the-s3-compatible-api)
- [APIReference](https://www.backblaze.com/docs/cloud-storage-call-the-s3-compatible-api)

## Common Properties

- [Website](https://www.backblaze.com)
- [Portal](https://www.backblaze.com/docs)
- [Documentation](https://www.backblaze.com/apidocs/)
- [GettingStarted](https://www.backblaze.com/docs/cloud-storage-native-api)
- [Pricing](https://www.backblaze.com/cloud-storage/pricing)
- [SignUp](https://www.backblaze.com/b2/sign-up.html)
- [Blog](https://www.backblaze.com/blog/)
- [StatusPage](https://status.backblaze.com)
- [Support](https://help.backblaze.com)
- [TermsOfService](https://www.backblaze.com/company/terms-of-service)
- [PrivacyPolicy](https://www.backblaze.com/company/privacy.html)
- [GitHubOrganization](https://github.com/Backblaze)
- [GitHubRepository](https://github.com/Backblaze/b2-sdk-python)
- [Python SDK (B2 CLI & SDK)](https://pypi.org/project/b2/)
- [Java SDK](https://github.com/Backblaze/b2-sdk-java)
- [Go SDK](https://github.com/Backblaze/blazer)
- [B2 Command Line Tool](https://github.com/Backblaze/B2_Command_Line_Tool)
- [Terraform Provider](https://github.com/Backblaze/terraform-provider-b2)

## Features

| Name | Description |
|------|-------------|
| Object Storage | Store and retrieve any amount of data with a simple flat namespace and unique file IDs. |
| S3-Compatible API | Use existing S3 tools and libraries without modification via the S3-compatible API endpoint. |
| Large File Multi-Part Upload | Upload files larger than 5GB using the multi-part upload API (b2_start_large_file / b2_upload_part / b2_finish_large_file). |
| Application Key Management | Create and manage scoped application keys with per-bucket and per-prefix restrictions. |
| Lifecycle Rules | Automatically delete or hide files after a specified number of days using lifecycle rules. |
| File Versioning | Keep multiple versions of files; older versions are preserved and accessible by file ID. |
| Event Notifications | Configure webhook-based event notifications when objects are created, modified, or deleted. |
| Object Lock | Protect files from deletion or modification for a specified retention period using object lock. |
| Cross-Region Replication | Replicate buckets to other regions or accounts for disaster recovery and data locality. |
| Server-Side Encryption | Encrypt data at rest using Backblaze-managed or customer-managed keys. |
| Cloudflare Bandwidth Alliance | Zero egress fees when serving B2 data through Cloudflare CDN. |

## Use Cases

| Name | Description |
|------|-------------|
| Application Data Storage | Store application data, user-uploaded content, and media files in the cloud. |
| Backup and Disaster Recovery | Use Backblaze B2 as the storage backend for backup tools like Arq, MSP360, and Veeam. |
| Media Hosting and Delivery | Host images, videos, and other media files and serve them via CDN integration. |
| Archival Storage | Store infrequently accessed archival data at low cost with lifecycle-based management. |
| Data Migration | Migrate data from S3 or other cloud storage providers using the S3-compatible API. |
| CI/CD Artifact Storage | Store build artifacts, logs, and deployment packages in B2 buckets. |

## Integrations

| Name | Description |
|------|-------------|
| Cloudflare | Zero egress bandwidth alliance for CDN delivery of B2 content. |
| Arq Backup | Popular Mac and Windows backup application with native B2 support. |
| Synology | Synology NAS Hyper Backup integration for cloud backup. |
| Veeam | Enterprise backup and replication solution with B2 support. |
| MSP360 | Managed backup service with native B2 storage support. |
| Terraform | Infrastructure as code support via the official Terraform provider. |
| rclone | Command-line sync tool with native B2 Native and S3-compatible API support. |

## Artifacts

Machine-readable API specifications organized by format.

### OpenAPI

- [Backblaze B2 Native API](openapi/backblaze-b2-native-api.yaml)

### JSON Schema

- [Authorize Account Response](json-schema/b2-native-api-authorize-account-response-schema.json)
- [Bucket](json-schema/b2-native-api-bucket-schema.json)
- [File Info](json-schema/b2-native-api-file-info-schema.json)
- [Application Key](json-schema/b2-native-api-application-key-schema.json)
- [Notification Rule](json-schema/b2-native-api-notification-rule-schema.json)
- [+ 37 more schemas](json-schema/)

### JSON Structure

- [Authorize Account Response](json-structure/b2-native-api-authorize-account-response-structure.json)
- [Bucket](json-structure/b2-native-api-bucket-structure.json)
- [File Info](json-structure/b2-native-api-file-info-structure.json)
- [+ 39 more structures](json-structure/)

### JSON-LD

- [Backblaze B2 JSON-LD Context](json-ld/backblaze-b2-context.jsonld)

## Capabilities

Naftiko capabilities organized as shared per-API definitions composed into customer-facing workflows.

### Shared Per-API Definitions

- [Backblaze B2 Native API](capabilities/shared/b2-native-api.yaml) — 22 operations for account authorization, bucket management, file operations, large file uploads, application key management, and event notifications

### Workflow Capabilities

| Workflow | APIs Combined | Tools | Persona |
|----------|--------------|-------|---------|
| [Cloud Storage Management](capabilities/cloud-storage-management.yaml) | B2 Native API | 24 | Developer, DevOps Engineer, Application Integrator |

## Vocabulary

- [Backblaze Vocabulary](vocabulary/backblaze-vocabulary.yaml) — Unified taxonomy mapping 6 resources, 15 actions, 1 workflow, and 3 personas across operational (OpenAPI) and capability (Naftiko) dimensions

## Rules

- [Backblaze Spectral Rules](rules/backblaze-spectral-rules.yml) — 30 rules across 8 categories enforcing Backblaze B2 API conventions

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
