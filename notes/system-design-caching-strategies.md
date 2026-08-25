# ⚡ System Design: Caching Strategies

Patterns for distributed caching in scalable architectures.

## Common Caching Patterns
1. **Cache-Aside (Lazy Loading)**: Application reads cache; if miss, reads database and populates cache.
2. **Write-Through**: Application writes to cache; cache immediately persists to database synchronously.
3. **Write-Behind (Write-Back)**: Application writes to cache; cache asynchronously writes to DB in batches.
4. **Refresh-Ahead**: Cache proactively re-fetches frequently accessed hot keys before TTL expiry.
