# 🌐 API Design: REST vs GraphQL

Comparative breakdown of API architecture paradigms.

| Aspect | RESTful APIs | GraphQL |
| :--- | :--- | :--- |
| **Data Fetching** | Multiple endpoints, over/under-fetching risk | Single endpoint, client requests exact fields |
| **Caching** | Native HTTP caching (ETags, CDN, Cache-Control) | Complex client-side normalized caching (Apollo, Urql) |
| **Versioning** | URI versioning (`/v1/users`) or header-based | Schema evolution by deprecating fields |
| **Tooling** | OpenAPI / Swagger | GraphiQL, Apollo Studio |
