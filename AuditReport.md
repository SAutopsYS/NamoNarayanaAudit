# Audit Report

**Client-facing master document** for the Namo Narayana public website audit.  
**Website:** https://namonarayana.com/  
**Audit evidence date:** 2026-07-30  
**Repository hardening:** Phase 21 (documentation only; findings unchanged)


## Executive Summary

Namo Narayana operates a Shopify D2C storefront for premium A2 Gir cow ghee. Public discovery covered **60** URLs. **Three** ghee SKUs are sellable and checkout entry works. The homepage and policy layer are not campaign-ready: sample products, inflated review claims, missing SEO foundations, refund placeholders, and an unreachable shipping policy remain open.

**Final verdict: Not ready for paid acquisition.**  
**P0 open: 12 · P0 Fixed: 0 · Governance gates: 4/17 PASS**


## Website Overview

| Item | Detail |
|------|--------|
| Brand | Namo Narayana |
| Platform | Shopify + Cloudflare |
| Primary catalog | A2 Gir Cow Bilona ghee (1L / 2.5L / 5L live) |
| Other SKUs | Published but largely unavailable at ₹0.00 |
| Locales observed | en / INR checkout path |


## Audit Objectives

1. Discover every public URL before reporting.  
2. Attach permanent Issue IDs and Evidence IDs.  
3. Deliver a GitHub-ready archive for client, portfolio, and maintenance.  
4. State readiness honestly without inventing lab scores or screenshots.


## Methodology

1. Crawl sitemaps and Shopify JSON APIs.  
2. Probe candidates for status, title, canonical, indexability.  
3. Evidence-fetch critical templates (home, PDP, collections, policies, search, cart).  
4. Register defects with permanent IDs (`FUNC`, `SEO`, `P`, `UX`, `ACC`, `PERF`, `ARCH`, `SEC`).  
5. Phase 21: restructure documentation only; **no new findings, no severity changes**.


## Scope

**In scope:** Public HTML/HTTP, robots/sitemaps, headers, catalog JSON.  
**Out of scope:** Admin, payment completion, exploit testing, unpublished theme previews.


## Discovery Summary

| Metric | Value |
|--------|------:|
| URLs probed | 60 |
| HTTP 200 | 50 |
| Unreachable | 10 |
| Products | 13 (3 available) |
| Collections | 9 (2 empty) |
| Content pages | 7 |
| Blog articles | 0 |

Details: [Discovery/DiscoveredPages.md](./Discovery/DiscoveredPages.md) · evidence **EV0001**


## Risk Summary

| Risk class | Severity | Drivers |
|------------|----------|---------|
| Trust / merchandising | Critical | FUNC0001, UX0001, UX0002, FUNC0002, FUNC0003 |
| Legal / policy | Critical | P0001, P0002, P0003 |
| SEO foundations | High | SEO0001-SEO0003, SEO0005 |
| Accessibility (observable) | High | SEO0001, ACC0001, ACC0002 |
| Performance hygiene | High | PERF0001, PERF0002 |
| Security hardening | Medium | SEC0001-SEC0003 (transport OK) |


## Findings Summary

Working path: search, cart, checkout entry, HTTPS/HSTS, robots/sitemap, three priced live ghee SKUs.

Failing path: homepage trust/SEO, refund content, shipping availability, FAQ, broken collection handles, empty/overlapping collections, missing JSON-LD, incomplete security headers.


## Issue Summary

| Severity | Open | Fixed |
|----------|-----:|------:|
| P0 | 12 | 0 |
| P1 | 16 | 0 |

Full register: [Registers/IssuesRegister.md](./Registers/IssuesRegister.md)  
ID map: [Registers/IssueIdMap.md](./Registers/IssueIdMap.md)


## Evidence Summary

| Availability | Count | IDs |
|--------------|------:|-----|
| Exists | 20 | EV0001-EV0016, EV0021-EV0024 |
| Missing | 4 | EV0017-EV0020 |
| Cannot Be Collected | 3 | EV0025-EV0027 |

SHA256 metadata: [Evidence/Metadata/](./Evidence/Metadata/).  
Browse: [EvidenceIndex.md](./EvidenceIndex.md) · Catalog: [EvidenceManifest.md](./EvidenceManifest.md).  
No screenshots or Lighthouse files were fabricated.


## Overall Status

| Dimension | Status |
|-----------|--------|
| Audit documentation | Complete |
| Evidence traceability | Complete for verified artifacts |
| Production readiness | **Not ready** |
| Paid ads | **Do not scale** |


## Recommendations

Execute [Reports/OperationsHandover.md](./Reports/OperationsHandover.md) steps 1-10, then re-probe and update RemediationValidation with new Evidence IDs before any status flips.


## Audit Timeline

Full stage history: [AuditTimeline.md](./AuditTimeline.md)

| Date | Event |
|------|-------|
| 2026-07-30 | Live discovery + evidence probes |
| 2026-07-30 | Working package `website-audit/` authored |
| 2026-07-30 | Phase 21 hardening → Phase 22 evidence → Knowledge Base Release |


## Repository Map

Full IA: [RepositoryMap.md](./RepositoryMap.md) · Clickable index: [NavigationIndex.md](./NavigationIndex.md)  
How to read: [ReviewerGuide.md](./ReviewerGuide.md) · Why we decided: [DecisionLog.md](./DecisionLog.md) · Chronology: [AuditTimeline.md](./AuditTimeline.md)

```
WebsiteAudit/
  README.md · AuditReport.md · knowledge-layer docs
  Discovery/ · Registers/ · Reports/ · Evidence/ · Standards/
```


## Final Conclusion

The store can accept checkout entry for three live ghee products. It cannot yet defend trust, policy completeness, or homepage SEO/accessibility basics. This repository preserves that conclusion with stable IDs and evidence links for remediation tracking.

