# ToolJet (tooljet)

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

ToolJet is an open-source low-code platform for building internal tools, dashboards, business applications, workflows, and AI agents. It provides a REST External API for programmatic management of users, workspaces, applications, and user roles across self-hosted and cloud deployments. Authentication uses a static access token configured via environment variables and passed as a Basic Authorization header. ToolJet supports connecting to dozens of external data sources — REST APIs, GraphQL, databases, cloud storage, and SaaS tools — and offers OpenAPI-spec-driven data source integration within the platform. Pricing spans a free tier (2 builders, 50 end users, 2 apps) through Pro, Team, and Enterprise plans, with self-hosted Community Edition available at no cost.

APIs.json: [https://raw.githubusercontent.com/api-evangelist/tooljet/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/tooljet/refs/heads/main/apis.yml)

Naftiko: [https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=tooljet-api-evangelist&utm_content=repo](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=tooljet-api-evangelist&utm_content=repo)

## Tags

- low-code
- internal tools
- open-source
- application builder
- workflow automation
- no-code
- dashboards
- AI agents

## APIs

### ToolJet External API

The ToolJet External API provides REST endpoints for managing users, workspaces, applications (export/import), and user role assignments across a ToolJet instance. Enabled via `ENABLE_EXTERNAL_API=true` environment variable and secured with a static `EXTERNAL_API_ACCESS_TOKEN` using Basic authentication.

- **Base URL:** `https://your-tooljet-instance.com/api/ext`
- **Auth:** Basic Authorization (static access token)
- **Documentation:** [https://docs.tooljet.com/docs/tooljet-api/](https://docs.tooljet.com/docs/tooljet-api/)

Key endpoints:

| Method | Endpoint | Purpose |
|--------|----------|---------|
| GET | `/api/ext/users` | Retrieve all users |
| POST | `/api/ext/users` | Create a new user |
| GET | `/api/ext/user/:id` | Get a specific user |
| PATCH | `/api/ext/user/:id` | Update user details |
| GET | `/api/ext/workspaces` | Retrieve all workspaces |
| GET | `/api/ext/workspace/:id/apps` | Get apps for a workspace |
| PUT | `/api/ext/update-user-role/workspace/:workspaceId` | Modify user role |
| PUT | `/api/ext/user/:id/workspaces` | Replace user workspace relations |
| PATCH | `/api/ext/user/:id/workspaces/:workspaceId` | Update workspace relation |
| POST | `/api/ext/export/workspace/:id/apps/:appId` | Export an application |
| POST | `/api/ext/import/workspace/:id/apps` | Import an application |

## Plans / Rate Limits / FinOps

- **Plans & Pricing:** [plans/tooljet-plans-pricing.yml](plans/tooljet-plans-pricing.yml)
- **Rate Limits:** [rate-limits/tooljet-rate-limits.yml](rate-limits/tooljet-rate-limits.yml)
- **FinOps:** [finops/tooljet-finops.yml](finops/tooljet-finops.yml)

### Pricing Summary

| Plan | Price | Builders | End Users | Apps |
|------|-------|----------|-----------|------|
| Free | $0/mo | 2 | 50 | 2 |
| Pro | $79/builder/mo | Unlimited | 100 | 5 |
| Team | $199/builder/mo | Unlimited | Unlimited | Unlimited |
| Enterprise | Custom | Custom | Custom | Unlimited |

Annual billing offers 20% discount on Pro and Team plans. Self-hosted Community Edition is free.

## Timestamps

- **Created:** 2026-06-12
- **Modified:** 2026-06-12

## Common Properties

| Type | URL |
|------|-----|
| Website | [https://tooljet.com/](https://tooljet.com/) |
| Documentation | [https://docs.tooljet.com/docs/](https://docs.tooljet.com/docs/) |
| GitHub Organization | [https://github.com/ToolJet](https://github.com/ToolJet) |
| LinkedIn | [https://www.linkedin.com/company/tooljet](https://www.linkedin.com/company/tooljet) |
| X (Twitter) | [https://x.com/tooljet](https://x.com/tooljet) |
| Blog | [https://blog.tooljet.com/](https://blog.tooljet.com/) |
| Pricing | [https://tooljet.com/pricing](https://tooljet.com/pricing) |
| Status Page | [https://status.tooljet.com/](https://status.tooljet.com/) |

## Maintainers

- **Kin Lane** — [kin@apievangelist.com](mailto:kin@apievangelist.com)
