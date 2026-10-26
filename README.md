# MX Technologies (mx-technologies)

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

MX Technologies is a financial data connectivity platform providing REST APIs for account aggregation, data cleansing, transaction categorization, and open banking connectivity across more than 16,000 financial institutions. The platform powers money experiences for over 2,000 banks, credit unions, and fintechs by turning raw, unstructured financial data into actionable intelligence. MX offers a suite of APIs built around FDX standards for permissioned open banking data sharing, with SDKs in Node.js, Python, Java, Ruby, and Go, plus a hosted Connect Widget for rapid deployment.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/mx-technologies/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/mx-technologies/refs/heads/main/apis.yml)

**Naftiko:** [https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=mx-technologies-api-evangelist&utm_content=repo](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=mx-technologies-api-evangelist&utm_content=repo)

## Tags

- Financial Data
- Account Aggregation
- Open Banking
- Data Connectivity
- Fintech
- Transaction Categorization
- Data Enhancement
- FDX
- Account Verification
- Personal Finance

## APIs

| API | Description |
|-----|-------------|
| MX Platform API | Primary REST API for account aggregation, transactions, budgets, and insights across 16,000+ institutions |
| MX Atrium API | Legacy financial data connectivity API supporting 48,000+ data connections |
| MX SSO API | Authentication API for user login and widget URL generation |
| MX Data Access API | FDX-compliant open banking API for permissioned data sharing with OAuth support |
| MX Batch API | Bulk operations and batch request processing |
| MX Reporting API | Reporting and analytics for platform integrations |

## Plans, Rate Limits, and FinOps

| Resource | File |
|----------|------|
| Plans and Pricing | [plans/mx-technologies-plans-pricing.yml](plans/mx-technologies-plans-pricing.yml) |
| Rate Limits | [rate-limits/mx-technologies-rate-limits.yml](rate-limits/mx-technologies-rate-limits.yml) |
| FinOps Framework | [finops/mx-technologies-finops.yml](finops/mx-technologies-finops.yml) |

**Pricing Model:** Enterprise contracts, custom pricing negotiated with sales. Average annual contract: $15,000–$90,000 (per Vendr, 2025). Development sandbox is free (100 users, top 15 institutions).

**Key Rate Limits:**
- GET: 2,000 requests/second per client
- POST/PUT: 750 requests/second per client
- DELETE: 150 requests/second per client
- Standard aggregation: 1 job per 3 hours per member
- Balance checks: 5 requests per 2 hours per member

## Timestamps

| Field | Value |
|-------|-------|
| Created | 2026-06-12 |
| Modified | 2026-06-12 |

## Common Properties

| Type | URL |
|------|-----|
| Website | https://www.mx.com/ |
| Documentation | https://docs.mx.com/ |
| GitHub Organization | https://github.com/mxenabled |
| OpenAPI Specification | https://github.com/mxenabled/openapi |
| LinkedIn | https://www.linkedin.com/company/mxenabled |
| X (Twitter) | https://x.com/mX |
| Blog | https://www.mx.com/blog/ |
| Pricing | https://www.mx.com/company/ |
| Status Page | https://status.mx.com |

## Maintainers

**Kin Lane** — [kin@apievangelist.com](mailto:kin@apievangelist.com)
