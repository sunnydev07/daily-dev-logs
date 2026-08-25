# 🛡️ Web Security: Headers, CSP & CORS

Essential browser security standards for modern applications.

## Critical HTTP Headers
- **Content-Security-Policy (CSP)**: Restricts sources from which scripts, styles, and assets can load.
- **Strict-Transport-Security (HSTS)**: Forces HTTPS connections for all subdomains.
- **X-Content-Type-Options**: 
osniff prevents MIME-type sniffing vulnerabilities.
- **X-Frame-Options**: DENY or SAMEORIGIN prevents clickjacking attacks.

## Understanding CORS
CORS is an enforcement mechanism by the **browser**, not the server. Preflight OPTIONS requests verify allowed origins, methods, and headers before executing complex cross-origin requests.
