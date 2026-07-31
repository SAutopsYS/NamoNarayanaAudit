# Evidence Manifest

Inventory of audit evidence for https://namonarayana.com/.  
**Primary capture date:** 2026-07-30  
**Phase 22:** Evidence collection / classification (no new audit findings)

## Status legend

| Status | Meaning |
|--------|---------|
| **Evidence Exists** | File present in repository; SHA256 recorded in Metadata |
| **Evidence Missing** | Not captured; collectable in a future pass |
| **Evidence Cannot Be Collected** | Out of engagement scope or technically unavailable this engagement |

Sidecar metadata: [Evidence/Metadata/](./Evidence/Metadata/) (`EV0001.md` …).  
Human index: [EvidenceIndex.md](./EvidenceIndex.md).  
Gaps: [EvidenceGapRegister.md](./EvidenceGapRegister.md).  
Collection rules: [EvidenceCollectionGuide.md](./EvidenceCollectionGuide.md).


## Classification summary

| Status | Count | IDs |
|--------|------:|-----|
| Evidence Exists | 20 | EV0001-EV0016 (incl. EV0012 alias), EV0021-EV0024 |
| Evidence Missing | 4 | EV0017-EV0020 |
| Evidence Cannot Be Collected | 3 | EV0025-EV0027 |


## Evidence Exists

| Evidence ID | Stored Path | Type | Capture Date | Related Issues | Related Reports | Availability |
|-------------|-------------|------|--------------|----------------|-----------------|--------------|
| EV0001 | Evidence/Discovery/DiscoveredPages.csv | CSV | 2026-07-30 | FUNC0004, P0002, FUNC0005, ARCH0001-ARCH0003, P0004 | DiscoveredPages, PageInventory | Evidence Exists |
| EV0002 | Evidence/Discovery/DiscoveredPages.json | JSON | 2026-07-30 | (same as EV0001) | DiscoveredPages | Evidence Exists |
| EV0003 | Evidence/Discovery/UrlCandidates.txt | TXT | 2026-07-30 | N/A | AuditPlan | Evidence Exists |
| EV0004 | Evidence/SEO/RobotsTxt.txt | TXT | 2026-07-30 | CTRL0008 | Seo, Security | Evidence Exists |
| EV0005 | Evidence/SEO/SitemapIndex.xml | XML | 2026-07-30 | CTRL0008 | Seo, DiscoveredPages | Evidence Exists |
| EV0006 | Evidence/SEO/SitemapProducts.xml | XML | 2026-07-30 | CTRL0007 | Seo, PageInventory | Evidence Exists |
| EV0007 | Evidence/SEO/SitemapPages.xml | XML | 2026-07-30 | CTRL0012 | Seo, PageInventory | Evidence Exists |
| EV0008 | Evidence/SEO/SitemapCollections.xml | XML | 2026-07-30 | ARCH0001, ARCH0002 | Seo, Architecture | Evidence Exists |
| EV0009 | Evidence/SEO/SitemapBlogs.xml | XML | 2026-07-30 | ARCH0003 | Seo | Evidence Exists |
| EV0010 | Evidence/Discovery/SitemapAgenticDiscovery.xml | XML | 2026-07-30 | N/A | DiscoveredPages | Evidence Exists |
| EV0011 | Evidence/Reports/TemplateEvidence.jsonl | JSONL | 2026-07-30 | FUNC/UX/SEO/P/ACC/PERF/SEC metric set | FunctionalTesting, Seo, Accessibility, Performance, Security, UiReview | Evidence Exists |
| EV0012 | Evidence/Reports/TemplateEvidence.jsonl | JSONL (alias of EV0011) | 2026-07-30 | IssuesRegister template citations | Multiple | Evidence Exists |
| EV0013 | Evidence/Headers/SecurityHeadersSummary.md | MD | 2026-07-30 | SEC0001-SEC0003, CTRL0002 | Security | Evidence Exists |
| EV0014 | Evidence/Home/HomeProbeNotes.md | MD | 2026-07-30 | FUNC0001, UX0001, UX0002, SEO0001-SEO0003, SEO0005, PERF0002 | UiReview, Seo, UxReview | Evidence Exists |
| EV0015 | Evidence/Products/LivePdpProbeNotes.md | MD | 2026-07-30 | SEO0003, ACC0001, CTRL0010 | Seo, Accessibility | Evidence Exists |
| EV0016 | Evidence/Policies/RefundPolicyProbeNotes.md | MD | 2026-07-30 | P0001, SEO0004 | Documentation, FunctionalTesting | Evidence Exists |
| EV0021 | Evidence/Checkout/CheckoutEntryNotes.md | MD | 2026-07-30 | CTRL0005, CTRL0006 | FunctionalTesting, Security | Evidence Exists |
| EV0022 | Evidence/Collections/CollectionInventoryNotes.md | MD | 2026-07-30 | ARCH0001, ARCH0002 | Architecture, UiReview | Evidence Exists |
| EV0023 | Evidence/Navigation/BrokenCollectionHandles.md | MD | 2026-07-30 | FUNC0004 | FunctionalTesting, Architecture | Evidence Exists |
| EV0024 | Evidence/Search/SearchProbeNotes.md | MD | 2026-07-30 | CTRL0004, PERF0001 | FunctionalTesting, ResponsiveTesting | Evidence Exists |

SHA256 values: see `Evidence/Metadata/<EvidenceID>.md`.


## Evidence Missing

| Evidence ID | Intended artifact | Type | Related Issues | Notes |
|-------------|-------------------|------|----------------|-------|
| EV0017 | Screenshots (home, PDP, policies, journeys) | PNG/JPEG | FUNC0001, UX0001, UX0002, P0001 | Evidence Not Yet Collected |
| EV0018 | axe / WAVE export | JSON/HTML | ACC0001, ACC0002 | Evidence Not Yet Collected |
| EV0019 | Lighthouse report | JSON/HTML/PDF | PERF0001, PERF0002, NV0001 | Evidence Not Yet Collected |
| EV0020 | Full page HTML archives | HTML | N/A | Metrics retained in EV0011 instead |


## Evidence Cannot Be Collected

| Evidence ID | Intended artifact | Related | Reason |
|-------------|-------------------|---------|--------|
| EV0025 | Contact form delivery proof | NV0004 | Inbox/submit verification out of public-probe scope |
| EV0026 | Payment completion proof | NV0005 | Checkout payment forbidden without buyer approval |
| EV0027 | HTTP status bodies for aborted URLs | NV0006, P0002, FUNC0005 | Connection closed before status body; UNREACHABLE recorded in EV0001 |


## Rules

1. Never invent PNG/JPEG/PDF/HAR files.  
2. Cite **Evidence IDs** in reports; paths are secondary.  
3. EV0012 aliases EV0011 (same SHA256).  
4. New files require Metadata + Manifest update before citation.

