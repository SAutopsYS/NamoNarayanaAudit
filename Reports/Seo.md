# SEO

## Purpose

Technical SEO assessment across discovered indexable HTML and meta resources.

## Scope

All 200 HTML URLs from EV0001, plus robots.txt and sitemaps. Rankings not measured.

## Methodology

Parse titles, meta, canonical, OG, JSON-LD on evidence set; inventory indexability from discovery.

## Verified Findings

Homepage lacks H1, meta description, JSON-LD, and og:image (**SEO0001**, **SEO0002**, **SEO0003**, **SEO0005**). JSON-LD is also absent on other sampled templates (**SEO0003**). Policy pages lack meta descriptions (**SEO0004**). Live PDP is stronger (meta + og:image + H1); CTRL0010. robots.txt and sitemap index exist; CTRL0008. Broken handles, empty collections, empty blog, and overlapping indexes create crawl waste (**FUNC0004**, **ARCH0001**, **ARCH0002**, **ARCH0003**). Homepage `10,000+` claim remains a trust/SEO integrity issue (**UX0002**).

## Evidence References

| Evidence ID | See |
|-------------|-----|
| EV0001 | ../Evidence/Discovery/DiscoveredPages.csv |
| EV0004 | ../Evidence/SEO/RobotsTxt.txt |
| EV0005 | ../Evidence/SEO/SitemapIndex.xml |
| EV0006-EV0009 | ../Evidence/SEO/Sitemap*.xml |
| EV0011 | ../Evidence/Reports/TemplateEvidence.jsonl |
| EV0014 | ../Evidence/Home/HomeProbeNotes.md |
| EV0015 | ../Evidence/Products/LivePdpProbeNotes.md |

Metadata: `../Evidence/Metadata/EV0004.md`, `EV0014.md`


## Risk Analysis

Root URL SEO failure dominates because it is the brand canonical.

## Business Impact

Organic and social previews underperform while misleading claims create policy risk.

## Recommendations

Fix homepage foundations first; unpublish thin URLs; add policy metas; implement Product/Organization schema.

## Related Issues

SEO0001, SEO0002, SEO0003, SEO0004, SEO0005, UX0002, FUNC0004, ARCH0001, ARCH0002, ARCH0003

## Related Evidence

EV0014, EV0004, EV0005

## Related Reports

Accessibility, Architecture, UxReview

## Conclusion

Technical SEO is incomplete for a commercial D2C root and catalog IA.
