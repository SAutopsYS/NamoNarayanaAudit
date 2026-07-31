# Discovered Pages

## Purpose

Complete public URL inventory for https://namonarayana.com/ produced before phase reporting.

## Scope

Sitemap index and child maps, Shopify `products.json` / `collections.json` / `pages.json`, utility seeds, footer harvest, HTTP probes of every candidate.

## Methodology

Public HTTP only. Connection-aborted URLs are recorded as unreachable rather than assumed HTTP 404 (see NV0006).

## Verified Findings

- **60** URLs probed on 2026-07-30  
- **50** returned HTTP 200  
- **10** unreachable (connection aborted)  
- Full row-level table retained in source working package and machine export **EV0001** / **EV0002**

Authoritative machine table: [../Evidence/Discovery/DiscoveredPages.csv](../Evidence/Discovery/DiscoveredPages.csv) (EV0001).

Human summary of classes:

| Class | Examples | Notes |
|-------|----------|-------|
| Homepage | `/` | 200; title `Namo Narayana` |
| Products | 13 `/products/*` | All 200 |
| Collections | 9 live + 4 bad handles | Bad handles unreachable |
| Pages | 7 in pages.json | FAQ/about alias unreachable |
| Policies | privacy, refund, terms 200; shipping + others unreachable | |
| Blog | `/blogs/news` | 200; zero articles |
| Commerce | cart, checkout entry, search | Checkout redirects to session URL |
| Meta | robots, sitemaps, agents.md, `.well-known/ucp` | 200 |

## Evidence References

EV0001, EV0002, EV0003, EV0004-EV0010

## Risk Analysis

Unreachable shipping and FAQ URLs create trust and support gaps even when commerce entry works.

## Business Impact

Broken or empty paths waste crawl budget and frustrate buyers before checkout.

## Recommendations

Maintain this inventory after every publish. Re-probe unreachable policy URLs weekly until stable.

## Related Issues

FUNC0004, FUNC0005, P0002, P0004, ARCH0001, ARCH0002, ARCH0003

## Related Evidence

EV0001, EV0002, EV0003

## Related Reports

PageInventory, AuditPlan, WebsiteDiscovery, Seo

## Conclusion

Public surface area is known and versioned. Reporting must cite this inventory rather than invent URLs.
