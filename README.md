# Benevity (benevity)

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
