# ⚛️ React Hooks & Performance Optimization

Guidelines on avoiding premature optimization while preventing unnecessary re-renders.

## When to use useMemo & useCallback
- **useMemo**: Cache expensive calculations (e.g. filtering/sorting 10,000 items).
- **useCallback**: Pass stable function references to memoized children wrapped with React.memo.

## Common Pitfall: Object Identity
`	sx
// ❌ Re-created on every render, breaking child memoization:
<Child config={{ theme: 'dark' }} />

// ✅ Memoized config:
const config = useMemo(() => ({ theme: 'dark' }), []);
<Child config={config} />
`
"@
    },
    @{
        File = "notes/api-design-rest-and-graphql.md"
        Msg = "docs(notes): add REST vs GraphQL architectural comparison"
        Content = @"
# 🌐 API Design: REST vs GraphQL

Comparative breakdown of API architecture paradigms.

| Aspect | RESTful APIs | GraphQL |
| :--- | :--- | :--- |
| **Data Fetching** | Multiple endpoints, over/under-fetching risk | Single endpoint, client requests exact fields |
| **Caching** | Native HTTP caching (ETags, CDN, Cache-Control) | Complex client-side normalized caching (Apollo, Urql) |
| **Versioning** | URI versioning (/v1/users) or header-based | Schema evolution by deprecating fields |
| **Tooling** | OpenAPI / Swagger | GraphiQL, Apollo Studio |
