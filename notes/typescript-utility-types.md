# 🔷 TypeScript Advanced Utility Types

A practical reference for transforming types in TypeScript.

## Key Utility Types

| Type | Description |
| :--- | :--- |
| Partial<T> | Makes all properties in T optional |
| Required<T> | Makes all properties in T required |
| Readonly<T> | Makes all properties in T read-only |
| Pick<T, K> | Selects a set of properties K from T |
| Omit<T, K> | Removes properties K from T |
| Record<K, T> | Constructs an object type with keys K and values T |

## Conditional Type Example

`	ypescript
type NonNullableType<T> = T extends null | undefined ? never : T;
`
"@
    },
    @{
        File = "notes/linux-curl-and-networking.md"
        Msg = "docs(notes): add Linux networking and cURL cheat sheet"
        Content = @"
# 🐧 Linux Networking & cURL Reference

Essential commands for debugging network connectivity and API endpoints.

## cURL Mastery

`ash
# Measure request timings (DNS, Connect, TTFB, Total)
curl -w "\nDNS: %{time_namelookup}s | Connect: %{time_connect}s | TTFB: %{time_starttransfer}s | Total: %{time_total}s\n" -o /dev/null -s https://api.github.com

# Follow redirects and inspect headers
curl -IL https://example.com

# Send JSON payload
curl -X POST https://httpbin.org/post -H "Content-Type: application/json" -d '{"status":"ok"}'
`
"@
    },
    @{
        File = "notes/sql-indexing-and-optimization.md"
        Msg = "docs(notes): add SQL indexing and query optimization tips"
        Content = @"
# 🗄️ SQL Indexing & Query Optimization

Best practices for relational database performance.

## Index Types
- **B-Tree Index**: Ideal for equality (=) and range queries (<, >, BETWEEN).
- **Hash Index**: Ultra-fast exact lookups, but does not support range scans.
- **GIN / GiST Index**: Excellent for JSONB, array fields, and full-text search (PostgreSQL).

## Optimization Rules of Thumb
1. Index columns used frequently in WHERE, JOIN, and ORDER BY clauses.
2. Avoid SELECT *; fetch only necessary columns to benefit from covering indexes.
3. Be mindful of column order in composite indexes (Leftmost Prefix Rule).
