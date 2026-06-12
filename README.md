# ToolJet (tooljet)

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
