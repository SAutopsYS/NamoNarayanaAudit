# Namo Narayana Website Audit

Final release of the public website audit knowledge base for **https://namonarayana.com/**.

**Start here:** [STARTHERE.md](./STARTHERE.md) · **Executive brief:** [ExecutiveSummary.md](./ExecutiveSummary.md) · **Full narrative:** [AuditReport.md](./AuditReport.md)

## What this project is

An enterprise documentation archive of a discovery-first public audit of the Namo Narayana Shopify storefront. It packages verified findings, evidence, decisions, recommendations, and repository governance for GitHub delivery, client handoff, portfolio demonstration, interview walkthroughs, and long-term maintenance.

## Why it exists

To give operators and stakeholders a single, traceable record of what was verified on the live site, what remains open, what evidence supports each claim, and how to remediate without inventing lab scores or screenshots.

## Website overview

### Business overview

Namo Narayana is a D2C brand positioned around traditional Bilona A2 Gir cow ghee and related natural foods. Public story pages describe purity and traditional process. Legal NAP presentation is inconsistent across privacy and footer (P0003).

### Products

| Class | Count | Notes |
|-------|------:|-------|
| Products in catalog JSON | 13 | Discovery inventory |
| Available / sellable | 3 | Pure A2 Gir Cow Ghee 1L / 2.5L / 5L with non-zero prices |
| Published unavailable | 10 | Mostly ₹0.00 stubs (FUNC0003) |

### Collections

Nine JSON collections including empty publishes (`natural-sweeteners`, `organic-oils`) and overlapping indexes (`all` / `all-products` / `ghee` / `pure-ghee-honey` / `frontpage`). Four bad handles were unreachable in discovery (FUNC0004).

### Pages

Seven pages in `pages.json` (about-us, our-story, farm-to-fork, certifications, careers, contact, social-media). FAQ is not published (FUNC0005). Blog index has zero articles (ARCH0003).

### Policies

Privacy, refund, and terms returned 200. Refund contains placeholder/apparel language (P0001). Shipping policy was unreachable while footer-linked (P0002).

### Architecture overview

Shopify Online Store theme (Refresh family) behind Cloudflare. Information-architecture debt is publish discipline (draft SKUs, empty collections), not platform incapability.

### Technology observations

Public stack signals: Shopify + Cloudflare; HTTPS with HSTS; customer login redirects to Shopify authentication; checkout enters Shopify Checkout session URLs.

### SEO overview

Homepage missing H1, meta description, JSON-LD, and og:image (SEO0001-SEO0003, SEO0005). robots.txt and sitemap index present. Live PDP meta/og stronger than home. Empty/overlapping collections create thin or duplicate browse paths.

### Accessibility overview

Homepage H1 count 0; empty alts on home/PDP samples; cart has two H1s. Keyboard/contrast tooling exports Missing (EV0018). Full WCAG certification not claimed.

### Performance overview

Homepage HTML approximately 591 KB with high script count; srcset absent on primary templates; lazy loading present. Lighthouse/CWV: **Not Quantified From Verified Evidence** (EV0019 Missing).

### Security overview

Transport controls present (HSTS; XFO/nosniff pattern). Referrer-Policy and Permissions-Policy missing; CSP minimal (SEC0001-SEC0003). Payment completion not tested (EV0026).

### UX overview

Commerce path works; trust on homepage fails (samples, `0+` counters, `10,000+` claim). Policy reassurance fails (refund/shipping).

### Functional overview

Search, cart, and checkout entry verified. Broken collection URLs, FAQ, and shipping availability fail. Form inbox delivery and payment completion not verified.

### Overall strengths

Working checkout entry for three live ghee SKUs; HTTPS/HSTS; search behaviors; robots/sitemap; structured documentation archive with Evidence IDs.

### Overall weaknesses

Homepage merchandising and social proof; policy completeness; primary SEO foundations; empty/broken category IA; missing visual/lab evidence pack.

### Overall risks

See [RiskRegister.md](./RiskRegister.md). Paid-traffic amplification of trust/legal gaps is rated **Critical** until P0 closure (DEC0003). Financial magnitude: **Not Quantified From Verified Evidence**.

### Overall recommendations

See [RecommendationsRegister.md](./RecommendationsRegister.md). Execute P0 REC0001-REC0013 before any paid scale-up.

### Overall maturity

Documentation knowledge base: high (final release). Live storefront publish maturity: low relative to premium brand positioning.

### Overall readiness

| Subject | Readiness |
|---------|-----------|
| Paid ads / campaign landing | **Not ready** |
| Documentation delivery | **Final release** |
| Client technical handoff | Ready with evidence-gap disclosure |

## Audit objective

Verify the public production website, record defects with permanent Issue IDs, attach Evidence IDs, and deliver a maintainable archive without inventing captures or scores.

## Audit methodology

1. Discover public URLs (sitemaps, Shopify JSON, seeds).  
2. Plan report coverage (AuditPlan).  
3. Probe templates; store machine evidence (EV0011).  
4. Register Issues and Decisions.  
5. Write domain Reports that cite IDs.  
6. Harden repository; classify evidence Exists/Missing/Cannot Be Collected.  
7. Add knowledge layer; run repository QA; publish this final folder.

## Repository structure

```text
NamoNarayanaAudit/
  STARTHERE.md
  README.md
  ExecutiveSummary.md
  AuditReport.md
  DecisionLog.md · AuditTimeline.md · ReviewerGuide.md
  RepositoryMap.md · NavigationIndex.md · RepositoryGlossary.md
  RepositoryLifecycle.md · RepositoryQAReview.md
  RepositoryValidation.md · RepositoryReleaseChecklist.md · RepositoryStatistics.md
  EvidenceManifest.md · EvidenceIndex.md · EvidenceGapRegister.md
  IssuesRegister.md · TraceabilityMatrix.md
  RecommendationsRegister.md · RiskRegister.md
  ChangeLog.md · License.md
  Discovery/ · Reports/ · Evidence/ · Registers/ · Standards/ · Assets/
```

Detail: [RepositoryMap.md](./RepositoryMap.md)

## Evidence structure

Evidence lives under `Evidence/<Domain>/` with Metadata SHA256 sidecars. Catalog: [EvidenceManifest.md](./EvidenceManifest.md). Browse: [EvidenceIndex.md](./EvidenceIndex.md). Gaps: [EvidenceGapRegister.md](./EvidenceGapRegister.md).

| Status | Count |
|--------|------:|
| Exists | 20 |
| Missing | 4 |
| Cannot Be Collected | 3 |

## Audit workflow

```text
Discover → Plan → Probe → Register Issues → Report → Validate → Decide → Release
```

Chronology: [AuditTimeline.md](./AuditTimeline.md)

## Issue workflow

Permanent IDs (`FUNC`, `SEO`, `P`, `UX`, `ACC`, `PERF`, `ARCH`, `SEC`) in [IssuesRegister.md](./IssuesRegister.md). Map: [Registers/IssueIdMap.md](./Registers/IssueIdMap.md). Close only with new Evidence IDs ([RepositoryLifecycle.md](./RepositoryLifecycle.md)).

## Evidence workflow

Capture → Metadata + SHA256 → Manifest → cite Evidence ID in Issues/Reports. Never invent PNG/Lighthouse/axe files ([EvidenceCollectionGuide.md](./EvidenceCollectionGuide.md)).

## Decision workflow

Major calls logged as `DECnnnn` in [DecisionLog.md](./DecisionLog.md) (example: DEC0003 Paid Ads Not Ready).

## Report index

All twenty domain reports: [NavigationIndex.md](./NavigationIndex.md#reports) · folder [Reports/](./Reports/)

## Evidence index

[EvidenceIndex.md](./EvidenceIndex.md) · [EvidenceManifest.md](./EvidenceManifest.md)

## Repository navigation

[STARTHERE.md](./STARTHERE.md) · [ReviewerGuide.md](./ReviewerGuide.md) · [NavigationIndex.md](./NavigationIndex.md)

## Website health dashboard

Numeric lab/field scores were **not** produced for Core Web Vitals or automated a11y. Where no verified 0-100 metric exists, the cell states **Not Quantified From Verified Evidence**.

| Dimension | Score (0-100) |
|-----------|----------------|
| Overall Health | Not Quantified From Verified Evidence |
| Overall Risk | Not Quantified From Verified Evidence (qualitative: **Critical** for paid ads; RiskRegister) |
| Overall Maturity (storefront publish) | Not Quantified From Verified Evidence |
| Functional | Not Quantified From Verified Evidence |
| UX | Not Quantified From Verified Evidence |
| Accessibility | Not Quantified From Verified Evidence |
| SEO | Not Quantified From Verified Evidence |
| Performance | Not Quantified From Verified Evidence |
| Security | Not Quantified From Verified Evidence |
| Architecture | Not Quantified From Verified Evidence |
| Documentation (repo QA mean ×10) | **87** (from RepositoryQAReview mean 8.7/10) |
| Governance (gates PASS ratio) | **24** (4 of 17 gates PASS → 4/17×100) |
| Evidence Coverage (Exists / defined IDs) | **74** (20 Exists of 27 defined EV IDs) |
| Repository Readiness (repo QA Architecture×10) | **90** |
| Client Delivery Readiness (repo QA×10) | **80** |
| Portfolio Readiness (repo QA×10) | **90** |
| Interview Readiness (repo QA×10) | **90** |

Qualitative website readiness (not a 0-100 invention): **Paid ads = Not ready**.

## Business impact summary

Critical conversion and legal risk from homepage trust defects and policy gaps. Opportunity: three live ghee SKUs + checkout entry. ROI figures: **Not Quantified From Verified Evidence**. Detail: [Reports/BusinessImpact.md](./Reports/BusinessImpact.md) · [RiskRegister.md](./RiskRegister.md)

## Repository statistics

| Metric | Value |
|--------|------:|
| Domain reports | 20 |
| Defect Issue IDs | 28 |
| Decision IDs | 12 |
| Evidence IDs defined | 27 |
| Evidence Exists | 20 |
| Markdown files (approx. at release) | See RepositoryStatistics.md |

Refresh: [RepositoryStatistics.md](./RepositoryStatistics.md)

## Final audit verdict

**Website:** Not ready for paid acquisition.  
**P0 Fixed:** 0 / 12.  
**Decision:** DEC0003.

## Repository QA verdict

**Needs Minor Documentation Updates** (RepositoryQAReview). Mean documentation quality 8.7/10. Website findings unchanged.

## Knowledge base overview

This folder is a Knowledge Base Release: narrative (AuditReport), decisions, timeline, reviewer onboarding, evidence catalog, issue/recommendation/risk registers, and lifecycle rules for future waves.

## How to reproduce

1. Read [Discovery/AuditPlan.md](./Discovery/AuditPlan.md).  
2. Use candidate list `Evidence/Discovery/UrlCandidates.txt`.  
3. Compare live probes to `Evidence/Home/HomeProbeNotes.md` (EV0014) and `Evidence/Reports/TemplateEvidence.jsonl` (EV0011).  
4. Follow [EvidenceCollectionGuide.md](./EvidenceCollectionGuide.md) for new captures.

## Known limitations

- Public HTTP only; no admin.  
- Screenshots / Lighthouse / axe: Missing (EV0017-EV0019).  
- Payment and form delivery: Cannot Be Collected this engagement (EV0025-EV0026).  
- Some URLs aborted before HTTP status bodies (EV0027).  
- No invented financial ROI.

## Future maintenance

[RepositoryLifecycle.md](./RepositoryLifecycle.md): append new Evidence IDs; update IssuesRegister only with fresh proof; log readiness changes in DecisionLog; tag releases in git.

## License

[License.md](./License.md)
