# Cloudimage (cloudimage)

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

Cloudimage (by Scaleflex) is an image and video optimization, resizing, and CDN service. Its core interface is a URL-based transformation API - you request an origin image through `https://{token}.cloudimg.io/{origin-url}` and apply resize, crop, format, compression, filter, and watermark operations via query parameters, delivered over a global multi-CDN. A companion Filerobot DAM provides a REST upload and asset-management API.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/cloudimage/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/cloudimage/refs/heads/main/apis.yml)

## Tags

- Image Optimization
- Image CDN
- Resizing
- Transformation
- DAM

## Timestamps

- **Created:** 2026-06-20
- **Modified:** 2026-06-20

## APIs

### Cloudimage Image Transformation (URL API)

URL-based, on-the-fly image transformation. Requests carry the origin image as a path on the `{token}.cloudimg.io` host and apply operations through query parameters - resize (w, h, func=crop|fit|cropfit|bound|boundmin|cover), gravity, crop coordinates, flip, rotate, trim, and rounded corners - with no backend changes required.

- **Human URL:** [https://docs.cloudimage.io/transformations/image-operations](https://docs.cloudimage.io/transformations/image-operations)
- **Base URL:** `https://{token}.cloudimg.io`

#### Tags

- Image
- Transformation
- Resizing
- URL API

#### Properties

- [Documentation](https://docs.cloudimage.io/transformations/image-operations)
- [API Reference](https://docs.cloudimage.io/implementation/url-api-implementation)
- [OpenAPI](openapi/cloudimage-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cloudimage.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cloudimage.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cloudimage Optimization & CDN API

Automatic format conversion (WebP, AVIF) via force_format/format, lossy and lossless compression via quality (q), color and effect filters (blur, sharpen, contrast, greyscale, pixellate), and image or text watermarks (wat, wat_url, wat_text), all delivered through a global multi-CDN (CloudFront, Akamai, Fastly, CDN Networks).

- **Human URL:** [https://docs.cloudimage.io/transformations/image-operations](https://docs.cloudimage.io/transformations/image-operations)
- **Base URL:** `https://{token}.cloudimg.io`

#### Tags

- Optimization
- CDN
- Compression
- Format

#### Properties

- [Documentation](https://www.cloudimage.io/)
- [API Reference](https://docs.cloudimage.io/transformations/image-operations)
- [OpenAPI](openapi/cloudimage-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cloudimage.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cloudimage.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cloudimage Video Transformation (URL API)

On-the-fly video processing and transcoding for short web clips (up to 500 MB, 4K, 60s) using the same URL model - resize (w, h, func), background fill, format selection (auto, mp4, webm, h264/h265/vp9), and bitrate control.

- **Human URL:** [https://docs.cloudimage.io/transformations/video-operations](https://docs.cloudimage.io/transformations/video-operations)
- **Base URL:** `https://{token}.cloudimg.io`

#### Tags

- Video
- Transcoding
- Transformation
- URL API

#### Properties

- [Documentation](https://docs.cloudimage.io/transformations/video-operations)
- [OpenAPI](openapi/cloudimage-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cloudimage.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cloudimage.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Filerobot DAM Upload & Asset API

REST upload and digital-asset-management API for the Filerobot DAM (the Scaleflex storage that backs Cloudimage). Authenticated with X-Filerobot-Key, it supports multipart and stream upload, plus file and folder list, detail, rename, move, delete, and metadata operations.

- **Human URL:** [https://developers.scaleflex.com/](https://developers.scaleflex.com/)
- **Base URL:** `https://api.filerobot.com/{token}/v4`

#### Tags

- DAM
- Upload
- Asset Management
- Filerobot

#### Properties

- [Documentation](https://developers.scaleflex.com/)
- [API Reference](https://docs.filerobot.com/go/filerobot-documentation/en/dam-api/file-api)
- [OpenAPI](openapi/cloudimage-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cloudimage.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cloudimage.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/scaleflex)
- [LinkedIn](https://www.linkedin.com/company/scaleflex)
- [Website](https://www.cloudimage.io/)
- [Documentation](https://docs.cloudimage.io/)
- [Plans](plans/cloudimage-plans-pricing.yml)
- [Rate Limits](rate-limits/cloudimage-rate-limits.yml)
- [Fin Ops](finops/cloudimage-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
