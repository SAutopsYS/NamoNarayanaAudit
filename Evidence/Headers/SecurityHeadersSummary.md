# Security Headers Summary

**Evidence ID:** EV0013  
**Source:** EV0011 header fields on HOME / PDP_LIVE / CART  
**Capture date:** 2026-07-30  
**No new live requests were made for this summary.**

| Header | Observed value (HOME) | Notes |
|--------|----------------------|-------|
| Strict-Transport-Security | max-age=7889238 | CTRL0002 |
| Content-Security-Policy | block-all-mixed-content; frame-ancestors 'none'; upgrade-insecure-requests; | SEC0003 |
| Referrer-Policy | (empty string in evidence log) | SEC0001 |
| Permissions-Policy | (empty string in evidence log) | SEC0002 |
| X-Frame-Options | DENY (confirmed in source audit header probes) | CTRL0003 |
| X-Content-Type-Options | nosniff (confirmed in source audit header probes) | CTRL0003 |
| Server | cloudflare | Informational |

Related issues: SEC0001, SEC0002, SEC0003.
