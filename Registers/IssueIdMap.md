# Issue ID Map

Permanent Issue IDs for this repository. Legacy `NN-###` IDs from the working audit package map 1:1. **Do not mint new IDs for the same defect.**

| Permanent ID | Legacy ID | Domain | Title | Severity |
|--------------|-----------|--------|-------|----------|
| FUNC0001 | NN-001 | Functional | Sample products on homepage | P0 |
| UX0001 | NN-002 | UX | Trust counters show `0+` | P0 |
| UX0002 | NN-003 | UX | Inflated “10,000+” reviews claim | P0 |
| SEO0001 | NN-004 | SEO | Homepage missing H1 | P0 |
| SEO0002 | NN-005 | SEO | Homepage meta description missing | P0 |
| SEO0003 | NN-006 | SEO | JSON-LD absent on sampled templates | P0 |
| P0001 | NN-007 | Policy | Refund policy placeholders / apparel template | P0 |
| P0002 | NN-008 | Policy | Shipping policy unreachable | P0 |
| FUNC0002 | NN-009 | Functional | Coming Soon clutter | P0 |
| FUNC0003 | NN-010 | Functional | Rs. 0.00 / zero-price catalog noise | P0 |
| FUNC0004 | NN-011 | Functional | Broken collection handles | P0 |
| FUNC0005 | NN-012 | Functional | FAQ unreachable / not in pages.json | P0 |
| SEO0004 | NN-013 | SEO | Policy pages missing meta descriptions | P1 |
| ACC0001 | NN-014 | Accessibility | Empty or missing image alt | P1 |
| PERF0001 | NN-015 | Performance | Missing srcset on key templates | P1 |
| PERF0002 | NN-016 | Performance | Heavy homepage payload | P1 |
| SEO0005 | NN-017 | SEO | Homepage missing og:image | P1 |
| P0003 | NN-018 | Policy | NAP inconsistency (Bhiwani vs Sonipat) | P1 |
| UX0003 | NN-019 | UX | Typo “Batch Teste” | P1 |
| FUNC0006 | NN-020 | Functional | Turmeric search chip without SKU | P1 |
| ARCH0001 | NN-021 | Architecture | Empty published collections | P1 |
| ARCH0002 | NN-022 | Architecture | Overlapping collection indexes | P1 |
| SEC0001 | NN-023 | Security | Missing Referrer-Policy | P1 |
| SEC0002 | NN-024 | Security | Missing Permissions-Policy | P1 |
| SEC0003 | NN-025 | Security | Weak Content-Security-Policy | P1 |
| P0004 | NN-026 | Policy | Additional policy URLs unreachable | P1 |
| ARCH0003 | NN-027 | Architecture | Blog index has zero articles | P1 |
| ACC0002 | NN-028 | Accessibility | Cart template has two H1 elements | P1 |

## Working controls (not defects)

| Control ID | Legacy | Description |
|------------|--------|-------------|
| CTRL0001 | NN-OK-01 | Homepage HTTP 200 |
| CTRL0002 | NN-OK-02 | HTTPS + HSTS |
| CTRL0003 | NN-OK-03 | X-Frame-Options DENY + nosniff |
| CTRL0004 | NN-OK-04 | Search hit and zero-result paths |
| CTRL0005 | NN-OK-05 | Cart page loads |
| CTRL0006 | NN-OK-06 | Checkout entry redirects to Shopify Checkout |
| CTRL0007 | NN-OK-07 | Three live ghee SKUs with non-zero prices |
| CTRL0008 | NN-OK-08 | robots.txt and sitemap index present |
| CTRL0009 | NN-OK-09 | Non-home sampled templates expose one H1 |
| CTRL0010 | NN-OK-10 | Live PDP has og:image and meta description |
| CTRL0011 | NN-OK-11 | Lazy loading present on homepage images |
| CTRL0012 | NN-OK-12 | Seven content pages published in pages.json |

## Not verifiable items

| ID | Legacy | Description |
|----|--------|-------------|
| NV0001 | NN-NV-01 | Lighthouse / CWV lab scores |
| NV0002 | NN-NV-02 | Keyboard focus visuals |
| NV0003 | NN-NV-03 | Contrast ratio measurements |
| NV0004 | NN-NV-04 | Contact form email delivery |
| NV0005 | NN-NV-05 | Payment authorization completion |
| NV0006 | NN-NV-06 | Definitive HTTP status for connection-aborted URLs |

## ID rules

1. Prefix denotes domain (`FUNC`, `SEO`, `SEC`, `UX`, `ACC`, `PERF`, `ARCH`, `P` for Policy).  
2. Numbers are zero-padded to four digits and never reused.  
3. One defect = one permanent ID. Cross-domain impact is expressed via Related Reports, not duplicate IDs.  
4. Legacy `NN-###` appears only in this map and Changelog for historical continuity.

