# Incode (incode)

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
