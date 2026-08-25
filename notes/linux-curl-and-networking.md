# 🐧 Linux Networking & cURL Reference

Essential commands for debugging network connectivity and API endpoints.

## cURL Diagnostics
```bash
curl -w "\nDNS: %{time_namelookup}s | Connect: %{time_connect}s | TTFB: %{time_starttransfer}s | Total: %{time_total}s\n" -o /dev/null -s https://api.github.com
curl -IL https://example.com
curl -X POST https://httpbin.org/post -H "Content-Type: application/json" -d '{"status":"ok"}'
```
