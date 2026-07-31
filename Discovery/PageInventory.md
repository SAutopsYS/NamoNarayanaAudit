# Page Inventory

## Purpose

Aggregate counts and structural observations derived from DiscoveredPages (EV0001) and Shopify JSON APIs.

## Scope

Products, collections, pages, policies, blog, duplicates, broken URLs, redirects.

## Methodology

Count by page type from discovery export; enrich with `products.json` availability/price and `collections.json` product counts recorded during the 2026-07-30 audit.

## Verified Findings

| Category | Count | Notes |
|----------|------:|-------|
| URLs probed | 60 | EV0001 |
| HTTP 200 | 50 | |
| Unreachable | 10 | |
| Products | 13 | 3 available (â‚¹2350 / â‚¹5550 / â‚¹10500) |
| Collections (JSON) | 9 | 2 empty (`natural-sweeteners`, `organic-oils`) |
| Content pages | 7 | No FAQ handle in pages.json |
| Blog articles | 0 | Index only |
| Redirects followed | 2 | login â†’ Shopify auth; checkout â†’ session URL |

### Broken / unreachable

`/collections/atta`, `/pickles`, `/natural-honey`, `/cold-pressed-oils`, `/pages/about`, `/pages/faq`, `/policies/shipping-policy`, `/policies/contact-information`, `/policies/legal-notice`, plus intentional 404 probe.

### Near-duplicate browse paths

`/collections/all` vs `/all-products`; `/ghee` vs `/pure-ghee-honey` vs `/frontpage`.

## Evidence References

EV0001, EV0006, EV0007, EV0008, EV0009

## Risk Analysis

Empty and overlapping collections dilute IA clarity (ARCH0001, ARCH0002).

## Business Impact

Customers and crawlers encounter thin or dead category paths beside a small live assortment.

## Recommendations

Unpublish empty collections; collapse overlapping indexes; fix or remove broken handles.

## Related Issues

FUNC0003, FUNC0004, ARCH0001, ARCH0002, ARCH0003, P0002, FUNC0005

## Related Evidence

EV0001, EV0008

## Related Reports

DiscoveredPages, Architecture, FunctionalTesting, Seo

## Conclusion

Inventory shows a thin sellable core (3 SKUs) inside a noisy published catalog.
