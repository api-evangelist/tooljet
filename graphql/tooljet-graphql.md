# ToolJet GraphQL API

ToolJet does not expose a native GraphQL management API of its own. Instead, it provides a **GraphQL data source connector** that allows ToolJet applications to connect to any external GraphQL endpoint and execute queries and mutations against it. The connector is configured per-application inside the ToolJet builder and supports multiple authentication schemes.

This document describes the GraphQL connector interface and the underlying ToolJet data model types that power the platform's REST External API.

## GraphQL Connector

The ToolJet GraphQL data source connector lets app builders connect ToolJet to any GraphQL API endpoint. Configuration happens at the data source level (base URL, authentication) and at the query level (operation body, variables, headers).

**Endpoint:** User-supplied GraphQL API endpoint (e.g. `https://api.example.com/graphql`)

**Documentation:** https://docs.tooljet.com/docs/data-sources/graphql

### Authentication Methods

| Method | Details |
|--------|---------|
| None | No credentials required |
| Basic | Username and password via HTTP Basic Auth |
| Bearer | JWT or static token passed as `Authorization: Bearer <token>` |
| OAuth 2.0 | Access token URL, client ID, client secret, scopes, and authorization URL |

### Request Configuration

Each ToolJet query against a GraphQL data source accepts:

- **Query / Mutation body** — the GraphQL operation string
- **Variables** — JSON key-value pairs substituted into the operation
- **Headers** — additional HTTP headers (e.g. `Content-Type`, `Authorization`)
- **URL Parameters** — query string parameters appended to the base URL
- **Cookies** — optional cookie values forwarded with the request

### Response

Query results are accessible in ToolJet via `{{queries.<queryname>.data}}`. Response metadata (status code, response headers, request details) is available at `{{queries.<queryname>.metadata}}`.

## ToolJet Data Model (GraphQL SDL)

The schema file `tooljet-schema.graphql` documents the core ToolJet platform types derived from the server-side TypeORM entities. These types represent the objects managed by the ToolJet External REST API and the internal platform.

**References:**
- Documentation: https://docs.tooljet.com/docs/data-sources/graphql
- GettingStarted: https://docs.tooljet.com/docs/tooljet-api/
- GitHub Source Entities: https://github.com/ToolJet/ToolJet/tree/main/server/src/entities
