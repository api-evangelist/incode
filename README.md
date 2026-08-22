# Incode (incode)

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

Incode is an AI-powered identity verification and biometric authentication platform. The Incode Omni API runs configurable onboarding sessions that capture and validate government IDs, perform face match and passive liveness, run government-database and watchlist/AML checks, and return scores, OCR data, and images via REST.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/incode/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/incode/refs/heads/main/apis.yml)

## Tags

- Identity Verification
- Biometrics
- KYC
- Liveness
- Onboarding

## Timestamps

- **Created:** 2026-06-25
- **Modified:** 2026-06-25

## APIs

### Incode Onboarding Sessions API

Creates and manages back-end onboarding sessions via POST /omni/start, returning a session token used to authorize all subsequent Omni module calls, and reports completion via GET /omni/finish-status.

- **Human URL:** [https://developer.incode.com/docs/onboarding-integration](https://developer.incode.com/docs/onboarding-integration)
- **Base URL:** `https://demo-api.incodesmile.com`

#### Tags

- Onboarding
- Sessions
- KYC

#### Properties

- [Documentation](https://developer.incode.com/docs/onboarding-integration)
- [API Reference](https://developer.incode.com/docs/api-onboarding-start-session)
- [OpenAPI](openapi/incode-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/incode.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/incode.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Incode ID Verification API

Captures and validates government IDs through POST /omni/add/front-id/v2, POST /omni/add/back-id/v2, and POST /omni/process/id, extracting OCR data and document authenticity scores from base64-encoded images.

- **Human URL:** [https://developer.incode.com/docs/api-onboarding-id-validation](https://developer.incode.com/docs/api-onboarding-id-validation)
- **Base URL:** `https://demo-api.incodesmile.com`

#### Tags

- ID Verification
- Document Capture
- OCR

#### Properties

- [Documentation](https://developer.incode.com/docs/api-onboarding-id-validation)
- [API Reference](https://developer.incode.com/reference/processid)
- [OpenAPI](openapi/incode-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/incode.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/incode.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Incode Face and Liveness API

Adds a selfie and runs passive liveness via POST /omni/add/face/third-party, then compares it against the ID portrait for face match via POST /omni/process/face.

- **Human URL:** [https://developer.incode.com/docs/api-onboarding-face-validation](https://developer.incode.com/docs/api-onboarding-face-validation)
- **Base URL:** `https://demo-api.incodesmile.com`

#### Tags

- Face Match
- Liveness
- Biometrics

#### Properties

- [Documentation](https://developer.incode.com/docs/api-onboarding-face-validation)
- [API Reference](https://developer.incode.com/reference/processface)
- [OpenAPI](openapi/incode-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/incode.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/incode.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Incode Government Validation API

Validates captured ID data against government databases (e.g. Mexico INE, Peru RENIEC) via POST /omni/process/government-validation, with optional fallback and selfie-to-government-image comparison.

- **Human URL:** [https://developer.incode.com/docs/government-verification](https://developer.incode.com/docs/government-verification)
- **Base URL:** `https://demo-api.incodesmile.com`

#### Tags

- Government Validation
- KYC
- Compliance

#### Properties

- [Documentation](https://developer.incode.com/docs/government-verification)
- [API Reference](https://developer.incode.com/reference/processgovernmentvalidation)
- [OpenAPI](openapi/incode-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/incode.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/incode.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Incode Watchlist and AML API

Screens individuals against global sanctions, PEP, and warning lists via POST /omni/process/global-watchlist and POST /omni/watchlist-result, with ongoing monitoring through GET /omni/updated-watchlist-result.

- **Human URL:** [https://developer.incode.com/docs/global-watchlist](https://developer.incode.com/docs/global-watchlist)
- **Base URL:** `https://demo-api.incodesmile.com`

#### Tags

- Watchlist
- AML
- Sanctions
- PEP

#### Properties

- [Documentation](https://developer.incode.com/docs/global-watchlist)
- [OpenAPI](openapi/incode-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/incode.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/incode.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Incode Results API

Retrieves onboarding results for a completed session by interview ID via GET /omni/get/score, GET /omni/get/ocr-data, and GET /omni/get/images.

- **Human URL:** [https://developer.incode.com/docs/how-to-fetch-onboarding-results-and-data](https://developer.incode.com/docs/how-to-fetch-onboarding-results-and-data)
- **Base URL:** `https://demo-api.incodesmile.com`

#### Tags

- Results
- Scores
- OCR

#### Properties

- [Documentation](https://developer.incode.com/docs/how-to-fetch-onboarding-results-and-data)
- [API Reference](https://developer.incode.com/docs/fetch-scores)
- [OpenAPI](openapi/incode-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/incode.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/incode.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Incode Webhooks API

Pushes onboarding status changes to a configured back-end URL; the ONBOARDING_FINISHED event signals that scores and data are ready to fetch, with a one-time retry on non-200 responses.

- **Human URL:** [https://developer.incode.com/docs/onboarding-status-webhook](https://developer.incode.com/docs/onboarding-status-webhook)
- **Base URL:** `https://demo-api.incodesmile.com`

#### Tags

- Webhooks
- Events
- Notifications

#### Properties

- [Documentation](https://developer.incode.com/docs/onboarding-status-webhook)
- [API Reference](https://developer.incode.com/docs/webhooks)
- [OpenAPI](openapi/incode-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

## Common Properties

- [GitHub Organization](https://github.com/Incode-Technologies-Example-Repos)
- [LinkedIn](https://www.linkedin.com/company/incodetech)
- [Website](https://incode.com)
- [Documentation](https://developer.incode.com/docs)
- [Plans](plans/incode-plans-pricing.yml)
- [Rate Limits](rate-limits/incode-rate-limits.yml)
- [Fin Ops](finops/incode-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
