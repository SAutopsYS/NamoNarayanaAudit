# Evidence Index

Browse verified evidence by domain. Prefer **Evidence IDs** in reports.

Example citation:

```text
Evidence: EV0014
See: Evidence/Home/HomeProbeNotes.md
Metadata: Evidence/Metadata/EV0014.md
```


## Home

| ID | Status | Path | Issues |
|----|--------|------|--------|
| EV0014 | Exists | [Evidence/Home/HomeProbeNotes.md](./Evidence/Home/HomeProbeNotes.md) | FUNC0001, UX0001, UX0002, SEO0001-SEO0003, SEO0005, PERF0002 |
| EV0017 | Missing |; (screenshots) | Evidence Missing (EV0017) |

Also covered in machine log **EV0011** (HOME row).


## Products

| ID | Status | Path | Issues |
|----|--------|------|--------|
| EV0015 | Exists | [Evidence/Products/LivePdpProbeNotes.md](./Evidence/Products/LivePdpProbeNotes.md) | SEO0003, ACC0001, CTRL0010 |
| EV0006 | Exists | [Evidence/SEO/SitemapProducts.xml](./Evidence/SEO/SitemapProducts.xml) | CTRL0007 |


## Collections

| ID | Status | Path | Issues |
|----|--------|------|--------|
| EV0022 | Exists | [Evidence/Collections/CollectionInventoryNotes.md](./Evidence/Collections/CollectionInventoryNotes.md) | ARCH0001, ARCH0002 |
| EV0008 | Exists | [Evidence/SEO/SitemapCollections.xml](./Evidence/SEO/SitemapCollections.xml) | ARCH0001, ARCH0002 |
| EV0023 | Exists | [Evidence/Navigation/BrokenCollectionHandles.md](./Evidence/Navigation/BrokenCollectionHandles.md) | FUNC0004 |


## Policies

| ID | Status | Path | Issues |
|----|--------|------|--------|
| EV0016 | Exists | [Evidence/Policies/RefundPolicyProbeNotes.md](./Evidence/Policies/RefundPolicyProbeNotes.md) | P0001, SEO0004 |
| EV0001 | Exists | [Evidence/Discovery/DiscoveredPages.csv](./Evidence/Discovery/DiscoveredPages.csv) | P0002, P0004, FUNC0005 (reachability) |
| EV0027 | Cannot Be Collected | N/A | Aborted policy URL bodies |


## SEO

| ID | Status | Path | Issues / Controls |
|----|--------|------|-------------------|
| EV0004 | Exists | [Evidence/SEO/RobotsTxt.txt](./Evidence/SEO/RobotsTxt.txt) | CTRL0008 |
| EV0005 | Exists | [Evidence/SEO/SitemapIndex.xml](./Evidence/SEO/SitemapIndex.xml) | CTRL0008 |
| EV0006 | Exists | SitemapProducts.xml | CTRL0007 |
| EV0007 | Exists | SitemapPages.xml | CTRL0012 |
| EV0008 | Exists | SitemapCollections.xml | ARCH0001, ARCH0002 |
| EV0009 | Exists | SitemapBlogs.xml | ARCH0003 |
| EV0014 | Exists | HomeProbeNotes.md | SEO0001-SEO0003, SEO0005 |
| EV0015 | Exists | LivePdpProbeNotes.md | SEO0003, CTRL0010 |


## Accessibility

| ID | Status | Path | Issues |
|----|--------|------|--------|
| EV0014 | Exists | HomeProbeNotes.md (h1=0, empty alt) | SEO0001, ACC0001 |
| EV0015 | Exists | LivePdpProbeNotes.md (empty alt) | ACC0001 |
| EV0011 | Exists | TemplateEvidence.jsonl (cart h1=2) | ACC0002 |
| EV0018 | Missing | axe/WAVE export | ACC0001, ACC0002 |


## Performance

| ID | Status | Path | Issues |
|----|--------|------|--------|
| EV0014 | Exists | HomeProbeNotes.md (bytes, scripts, srcset) | PERF0001, PERF0002 |
| EV0011 | Exists | TemplateEvidence.jsonl | PERF0001, PERF0002 |
| EV0024 | Exists | SearchProbeNotes.md (srcset contrast) | PERF0001 |
| EV0019 | Missing | Lighthouse report | PERF0001, PERF0002, NV0001 |


## Security

| ID | Status | Path | Issues |
|----|--------|------|--------|
| EV0013 | Exists | [Evidence/Headers/SecurityHeadersSummary.md](./Evidence/Headers/SecurityHeadersSummary.md) | SEC0001-SEC0003, CTRL0002 |
| EV0021 | Exists | [Evidence/Checkout/CheckoutEntryNotes.md](./Evidence/Checkout/CheckoutEntryNotes.md) | CTRL0006 |
| EV0026 | Cannot Be Collected | Payment completion proof | NV0005 |

Pointer: [Evidence/Security/SecurityEvidencePointer.md](./Evidence/Security/SecurityEvidencePointer.md)


## Discovery

| ID | Status | Path | Notes |
|----|--------|------|-------|
| EV0001 | Exists | DiscoveredPages.csv | Master URL table |
| EV0002 | Exists | DiscoveredPages.json | JSON twin |
| EV0003 | Exists | UrlCandidates.txt | Pre-probe list |
| EV0010 | Exists | SitemapAgenticDiscovery.xml | agents.md |
| EV0023 | Exists | BrokenCollectionHandles.md | Navigation dead ends |


## Search / Checkout / Navigation (supporting)

| ID | Status | Path |
|----|--------|------|
| EV0024 | Exists | Evidence/Search/SearchProbeNotes.md |
| EV0021 | Exists | Evidence/Checkout/CheckoutEntryNotes.md |
| EV0023 | Exists | Evidence/Navigation/BrokenCollectionHandles.md |


## Machine log (cross-cutting)

| ID | Status | Path |
|----|--------|------|
| EV0011 / EV0012 | Exists | Evidence/Reports/TemplateEvidence.jsonl |


## Missing / Cannot Be Collected (index)

See [EvidenceManifest.md](./EvidenceManifest.md) sections for EV0017-EV0020 and EV0025-EV0027.

