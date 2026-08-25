# 🗄️ SQL Indexing & Query Optimization

Best practices for relational database performance.

## Index Types
- **B-Tree Index**: Ideal for equality (`=`) and range queries (`<`, `>`, `BETWEEN`).
- **Hash Index**: Ultra-fast exact lookups, but does not support range scans.
- **GIN / GiST Index**: Excellent for JSONB, array fields, and full-text search (PostgreSQL).

## Optimization Rules
1. Index columns used frequently in `WHERE`, `JOIN`, and `ORDER BY` clauses.
2. Avoid `SELECT *`; fetch only necessary columns to benefit from covering indexes.
3. Be mindful of column order in composite indexes (Leftmost Prefix Rule).
