# Issues Register

**Website:** https://namonarayana.com/  
**Audit date:** 2026-07-30  
**ID authority:** [IssueIdMap.md](./IssueIdMap.md)  
**Evidence authority:** [../EvidenceManifest.md](../EvidenceManifest.md)  
**Traceability:** [TraceabilityMatrix.md](./TraceabilityMatrix.md)  
**Decisions affecting severity policy:** [../DecisionLog.md](../DecisionLog.md) (DEC0002, DEC0007)  
**Reader onboarding:** [../ReviewerGuide.md](../ReviewerGuide.md)

Status legend: ✅ Fixed · 🟡 Improved · ❌ Still Exists · ⚪ Not Verifiable

This register is the single source of truth for defects. Reports cite IDs; they do not redefine severity or status.


## P0 issues

### FUNC0001: Sample products on homepage
| Field | Value |
|-------|-------|
| Affected URLs | `https://namonarayana.com/` |
| Evidence | EV0012 |
| Severity | P0 |
| Business Impact | Staging-like catalog undermines premium trust and paid landing quality |
| Recommendation | Unpublish sample products; remove from homepage sections |
| Current Status | ❌ Still Exists |
| Previous Status | ❌ Still Exists |
| Reports | FunctionalTesting, UiReview, UxReview, RemediationValidation |

### UX0001: Trust counters show `0+`
| Field | Value |
|-------|-------|
| Affected URLs | `/` (primary); residual on other chrome |
| Evidence | EV0012 |
| Severity | P0 |
| Business Impact | Empty social proof weakens conversion confidence |
| Recommendation | Remove counters until real metrics exist |
| Current Status | ❌ Still Exists |
| Previous Status | ❌ Still Exists |
| Reports | UxReview, Seo, RemediationValidation |

### UX0002: Inflated “10,000+” reviews claim
| Field | Value |
|-------|-------|
| Affected URLs | `/` |
| Evidence | EV0012 |
| Severity | P0 |
| Business Impact | Misleading claim risk for advertising and brand trust |
| Recommendation | Align claims to review-app / PDP source of truth |
| Current Status | ❌ Still Exists |
| Previous Status | ❌ Still Exists |
| Reports | UxReview, Seo, BusinessImpact, RemediationValidation |

### SEO0001: Homepage missing H1
| Field | Value |
|-------|-------|
| Affected URLs | `/` |
| Evidence | EV0012 |
| Severity | P0 |
| Business Impact | Primary landing URL fails basic SEO and heading structure |
| Recommendation | Add one clear brand or product H1 |
| Current Status | ❌ Still Exists |
| Previous Status | ❌ Still Exists |
| Reports | Seo, Accessibility, RemediationValidation |

### SEO0002: Homepage meta description missing
| Field | Value |
|-------|-------|
| Affected URLs | `/` |
| Evidence | EV0012 |
| Severity | P0 |
| Business Impact | Weak control of search snippets |
| Recommendation | Write a unique 150-160 character description |
| Current Status | ❌ Still Exists |
| Previous Status | ❌ Still Exists |
| Reports | Seo, RemediationValidation |

### SEO0003: JSON-LD absent on sampled templates
| Field | Value |
|-------|-------|
| Affected URLs | `/`, live PDP, collections, contact, policies, blog (sampled set) |
| Evidence | EV0012 |
| Severity | P0 |
| Business Impact | No Product/Organization structured data for rich results |
| Recommendation | Implement Organization and Product JSON-LD |
| Current Status | ❌ Still Exists |
| Previous Status | ❌ Still Exists |
| Reports | Seo, Architecture, RemediationValidation |

### P0001: Refund policy placeholders / apparel template
| Field | Value |
|-------|-------|
| Affected URLs | `/policies/refund-policy` |
| Evidence | EV0012 |
| Severity | P0 |
| Business Impact | Invalid legal copy for a food brand |
| Recommendation | Rewrite for ghee/food returns; publish real return address |
| Current Status | ❌ Still Exists |
| Previous Status | ❌ Still Exists |
| Reports | FunctionalTesting, Documentation, OperationsHandover |

### P0002: Shipping policy unreachable
| Field | Value |
|-------|-------|
| Affected URLs | `/policies/shipping-policy` (footer-linked) |
| Evidence | EV0001, EV0012 |
| Severity | P0 |
| Business Impact | Buyers cannot review shipping terms |
| Recommendation | Publish a stable HTTP 200 shipping policy |
| Current Status | ❌ Still Exists |
| Previous Status | ❌ Still Exists |
| Reports | FunctionalTesting, Documentation, OperationsHandover |

### FUNC0002: Coming Soon clutter
| Field | Value |
|-------|-------|
| Affected URLs | `/`, `/collections/all-products`, other collections |
| Evidence | EV0012 |
| Severity | P0 |
| Business Impact | Storefront reads unfinished |
| Recommendation | Hide draft merchandising from customer surfaces |
| Current Status | ❌ Still Exists |
| Previous Status | ❌ Still Exists |
| Reports | UiReview, UxReview, Performance |

### FUNC0003: Rs. 0.00 / zero-price catalog noise
| Field | Value |
|-------|-------|
| Affected URLs | `/`; sitewide chrome; products.json unavailable SKUs |
| Evidence | EV0012, EV0001 |
| Severity | P0 |
| Business Impact | Price integrity failure |
| Recommendation | Draft unavailable SKUs; feature only priced live products |
| Current Status | ❌ Still Exists |
| Previous Status | ❌ Still Exists |
| Reports | FunctionalTesting, UiReview, Architecture |

### FUNC0004: Broken collection handles
| Field | Value |
|-------|-------|
| Affected URLs | `/collections/natural-honey`, `/cold-pressed-oils`, `/atta`, `/pickles` |
| Evidence | EV0001, EV0023 |
| Severity | P0 |
| Business Impact | Dead ends in browse paths |
| Recommendation | Point navigation to live handles or remove links |
| Current Status | ❌ Still Exists |
| Previous Status | ❌ Still Exists |
| Reports | FunctionalTesting, Seo, Architecture |

### FUNC0005: FAQ unreachable / not in pages.json
| Field | Value |
|-------|-------|
| Affected URLs | `/pages/faq` |
| Evidence | EV0001, EV0012 |
| Severity | P0 |
| Business Impact | Support content gap |
| Recommendation | Publish FAQ or remove FAQ references |
| Current Status | ❌ Still Exists |
| Previous Status | ❌ Still Exists |
| Reports | FunctionalTesting, Documentation, CompanyResearch |


## P1 issues

| ID | Title | Evidence | Status | Reports |
|----|-------|----------|--------|---------|
| SEO0004 | Policy pages missing meta descriptions | EV0012 | ❌ Still Exists | Seo, Documentation |
| ACC0001 | Empty or missing image alt | EV0012 | ❌ Still Exists | Accessibility, Seo |
| PERF0001 | Missing srcset on key templates | EV0012 | ❌ Still Exists | Performance, ResponsiveTesting |
| PERF0002 | Heavy homepage payload | EV0012 | ❌ Still Exists | Performance, ResponsiveTesting |
| SEO0005 | Homepage missing og:image | EV0012 | ❌ Still Exists | Seo |
| P0003 | NAP inconsistency (Bhiwani vs Sonipat) | EV0012 | ❌ Still Exists | CompanyResearch, Documentation |
| UX0003 | Typo “Batch Teste” | EV0012 | ❌ Still Exists | UiReview |
| FUNC0006 | Turmeric chip without SKU | EV0012 | ❌ Still Exists | FunctionalTesting |
| ARCH0001 | Empty published collections | EV0001 | ❌ Still Exists | Architecture, PageInventory |
| ARCH0002 | Overlapping collection indexes | EV0001 | ❌ Still Exists | Architecture, Seo |
| SEC0001 | Missing Referrer-Policy | EV0012 | ❌ Still Exists | Security |
| SEC0002 | Missing Permissions-Policy | EV0012 | ❌ Still Exists | Security |
| SEC0003 | Weak Content-Security-Policy | EV0012 | ❌ Still Exists | Security |
| P0004 | Additional policy URLs unreachable | EV0001 | ❌ Still Exists | Documentation |
| ARCH0003 | Blog index has zero articles | EV0001 | ❌ Still Exists | Architecture, Seo |
| ACC0002 | Cart has two H1 elements | EV0012 | ❌ Still Exists | Accessibility, UiReview |


## Summary counts

| Bucket | Count |
|--------|------:|
| P0 open | 12 |
| P1 open | 16 |
| P0 Fixed | 0 |
| Working controls | 12 |
| Not Verifiable | 6 |

