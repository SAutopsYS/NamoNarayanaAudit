# Architecture

## Purpose

Describe information-architecture and publish discipline issues on the Shopify storefront.

## Scope

Collection overlap/empties, global chrome leakage of draft products, missing structured data layer, empty blog.

## Methodology

Inventory analysis (EV0001) plus sitewide chrome metrics from EV0011 on non-home templates.

## Verified Findings

Overlapping catalog indexes (**ARCH0002**). Empty published collections (**ARCH0001**). Broken handles outside the live set (**FUNC0004**). Draft pricing leaks into global chrome (~Rs. 0.00 matches on contact/about/policies) (**FUNC0003**). No JSON-LD layer (**SEO0003**). Blog index has zero articles (**ARCH0003**).

## Evidence References

| Evidence ID | See |
|-------------|-----|
| EV0001 | ../Evidence/Discovery/DiscoveredPages.csv |
| EV0008 | ../Evidence/SEO/SitemapCollections.xml |
| EV0011 | ../Evidence/Reports/TemplateEvidence.jsonl |
| EV0022 | ../Evidence/Collections/CollectionInventoryNotes.md |
| EV0023 | ../Evidence/Navigation/BrokenCollectionHandles.md |

Metadata: `../Evidence/Metadata/EV0022.md`, `EV0023.md`


## Risk Analysis

Platform capability is fine; publish discipline is the defect class.

## Business Impact

IA noise competes with the three live SKUs that actually drive revenue.

## Recommendations

Freeze IA around sellable ghee; unpublish empties; remove bad handles; add schema.

## Related Issues

ARCH0001, ARCH0002, ARCH0003, FUNC0003, FUNC0004, SEO0003

## Related Evidence

EV0001, EV0008

## Related Reports

PageInventory, Seo, WebsiteDiscovery

## Conclusion

Shopify architecture is sound; information architecture needs cleanup.
