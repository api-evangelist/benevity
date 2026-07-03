# Benevity (benevity)

Benevity is a Calgary-based corporate purpose software platform for workplace giving, matching, grantmaking, and employee/customer volunteering. Its Giving API lets partners embed nonprofit-of-choice donations, optional matching, and charitable gift cards into e-commerce, banking, and rewards experiences; the Cause Search API exposes Benevity's vetted global nonprofit database; the Spark API lets existing Spark Employee Engagement clients surface giving and volunteering opportunities in other interfaces; and the Location Services API lets clients manage locations (stores, franchises, offices) inside the Benevity ecosystem.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/benevity/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/benevity/refs/heads/main/apis.yml)

## Access model

Benevity's API documentation at [developer.benevity.org](https://developer.benevity.org/) is publicly readable and follows the RESTful/OpenAPI standard, but **credentials are partner-gated**. There is no self-serve signup or public price list - a prospective integrator requests a demo through [benevity.com/request-a-demo](https://www.benevity.com/request-a-demo), and Benevity provisions OAuth 2.0 client credentials (and sandbox access at `api.benevity-staging.org`) as part of a negotiated client/partner agreement. The Spark API specifically is scoped to organizations that are already Spark Employee Engagement clients.

This entry documents the real, publicly-described API surface (paths, parameters, hosts, auth flow) as found in Benevity's own guides. It does not fabricate endpoints beyond what is documented; where a surface (Location Services) wasn't independently confirmed down to exact request/response schemas, it's flagged as `endpointsModeled` in `review.yml` rather than given a fabricated OpenAPI/collection entry.

## Tags

- Corporate Social Responsibility
- Workplace Giving
- Donations
- Volunteering
- Nonprofits
- Matching Gifts
- CSR
- ESG

## Timestamps

- **Created:** 2026-07-03
- **Modified:** 2026-07-03

## APIs

### Benevity Causes API

Search the Benevity Cause Database - a global directory of vetted, registered nonprofits - by keyword, location, NTEE category, country/state, and geographic proximity, with pagination and eligibility (match/donate/program/nominate) filtering on each result.

- **Human URL:** [https://developer.benevity.org/guides/causes/search-cause](https://developer.benevity.org/guides/causes/search-cause)
- **Base URL:** `https://skyline.benevity.org`

#### Properties

- [Documentation](https://developer.benevity.org/guides/)
- [API Reference](https://developer.benevity.org/guides/causes/search-cause)
- [OpenAPI](openapi/benevity-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/benevity.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/benevity.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Benevity Giving API

Route nonprofit-of-choice donations into digital experiences - e-commerce, online banking, rewards programs, and charitable gift cards. Postpaid company donations settle monthly against a donation report; prepaid donations are captured immediately by credit card (via a BlueSnap-backed tokenized payment flow), with optional company/peer matching and Gift Aid (UK) handling.

- **Human URL:** [https://developer.benevity.org/guides/giving/](https://developer.benevity.org/guides/giving/)
- **Base URL:** `https://skyline.benevity.org`

#### Properties

- [Documentation - Postpaid Donations](https://developer.benevity.org/guides/giving/post-paid-donations/)
- [Documentation - Prepaid Donations](https://developer.benevity.org/guides/giving/pre-paid-donations/)
- [OpenAPI](openapi/benevity-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/benevity.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/benevity.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Benevity Receipts API

Retrieve the PDF receipt for a completed donation by its backend receipt ID, or request that the receipt be emailed to the donor. Receipts show issue date, donor name/address, amount, and the disbursing foundation partner.

- **Human URL:** [https://developer.benevity.org/guides/giving/get-receipt.html](https://developer.benevity.org/guides/giving/get-receipt.html)
- **Base URL:** `https://skyline.benevity.org`

#### Properties

- [Documentation](https://developer.benevity.org/guides/giving/get-receipt.html)
- [OpenAPI](openapi/benevity-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/benevity.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/benevity.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Benevity Spark Giving Opportunities API

For existing Spark Employee Engagement clients - search a company's active giving opportunities (initiatives that route donations to one or more causes) by keyword and geographic proximity, for display on an intranet or in a communication-tool integration.

- **Human URL:** [https://developer.benevity.org/guides/spark-api/search-giveops.html](https://developer.benevity.org/guides/spark-api/search-giveops.html)
- **Base URL:** `https://api.benevity.org`

#### Properties

- [Documentation](https://developer.benevity.org/guides/spark-api/overview.html)
- [API Reference](https://developer.benevity.org/guides/spark-api/search-giveops.html)
- [OpenAPI](openapi/benevity-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/benevity.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/benevity.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Benevity Spark Volunteer Opportunities API

For existing Spark Employee Engagement clients - search a company's volunteer opportunities/events by keyword, date range, open shift spots, interests, skills, and whether the opportunity is ongoing or time-bounded.

- **Human URL:** [https://developer.benevity.org/guides/spark-api/search-volops.html](https://developer.benevity.org/guides/spark-api/search-volops.html)
- **Base URL:** `https://api.benevity.org`

#### Properties

- [Documentation](https://developer.benevity.org/guides/spark-api/overview.html)
- [API Reference](https://developer.benevity.org/guides/spark-api/search-volops.html)
- [OpenAPI](openapi/benevity-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/benevity.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/benevity.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Benevity Location Services API

Create and manage locations (stores, franchises, offices) inside the Benevity ecosystem - address data, contact information, and tags - so multi-location organizations can attribute giving and volunteering activity to a specific site. JWT-authenticated with the `api.locations` scope, JSON:API content type, URI-versioned (v1 current). As of the review date this API is documented as integrated only with the Versaic community investment platform; exact request/response schemas beyond the overview guide were not independently confirmed, so no OpenAPI or collection artifact was generated for it (`endpointsModeled` - see `review.yml`).

- **Human URL:** [https://developer.benevity.org/guides/location-api/overview.html](https://developer.benevity.org/guides/location-api/overview.html)
- **Base URL:** `https://api.benevity.org`

#### Properties

- [Documentation](https://developer.benevity.org/guides/location-api/overview.html)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/benevity)
- [Website](https://benevity.com)
- [Documentation](https://developer.benevity.org/)
- [Plans](plans/benevity-plans-pricing.yml)
- [Rate Limits](rate-limits/benevity-rate-limits.yml)
- [Fin Ops](finops/benevity-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
