# Website Discovery

## Purpose

Architecture summary of the live Shopify storefront. Detailed URL tables live in Discovery/, not here.

## Scope

Platform signals, catalog shape, policy surface, commerce entry points.

## Methodology

Synthesize EV0001 inventory and Shopify JSON counts recorded in PageInventory.

## Verified Findings

Stack is Shopify behind Cloudflare. Catalog contains 13 products with only three available. Nine collections include two empty publishes. Seven content pages are live; shipping policy and FAQ are unreachable. Cart loads; checkout enters Shopify Checkout. Blog index has no articles.

## Evidence References

| Evidence ID | See |
|-------------|-----|
| EV0001 | ../Evidence/Discovery/DiscoveredPages.csv |
| EV0005 | ../Evidence/SEO/SitemapIndex.xml |
| EV0006-EV0009 | ../Evidence/SEO/Sitemap*.xml |

Metadata: `../Evidence/Metadata/EV0001.md`


## Risk Analysis

Structural publish noise (empties, broken handles, missing policies) sits on top of a working checkout path.

## Business Impact

Buyers can purchase live ghee SKUs but encounter unfinished category and policy surfaces.

## Recommendations

See Architecture and OperationsHandover for IA cleanup sequencing.

## Related Issues

FUNC0003, FUNC0004, FUNC0005, P0002, ARCH0001, ARCH0002, ARCH0003

## Related Evidence

EV0001

## Related Reports

DiscoveredPages, PageInventory, Architecture

## Conclusion

Discovery is complete and versioned; remediation targets are URL-specific.
