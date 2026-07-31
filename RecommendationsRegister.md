# Recommendations Register

Actionable recommendations drawn only from verified IssuesRegister and OperationsHandover content.  
No new findings. Severities unchanged.

Status values mirror IssuesRegister: ❌ Still Exists until revalidated with new Evidence IDs.

## P0 recommendations (execute first)

| Rec ID | Issue ID | Recommendation | Acceptance signal | Owner report |
|--------|----------|----------------|-------------------|--------------|
| REC0001 | FUNC0001 | Unpublish sample products; remove from homepage sections | Homepage `Sample Product` count = 0 | OperationsHandover |
| REC0002 | FUNC0002 | Hide Coming Soon merchandising from customer surfaces | Homepage Coming Soon density cleared | OperationsHandover |
| REC0003 | FUNC0003 | Draft unavailable/₹0 SKUs; feature only priced live products | No Rs. 0.00 on primary surfaces | OperationsHandover |
| REC0004 | UX0001 | Remove `0+` trust counters until real metrics exist | No `0+` matches on `/` | OperationsHandover |
| REC0005 | UX0002 | Align review claims to app/PDP source of truth | No unverified `10,000+` claim on `/` | OperationsHandover |
| REC0006 | SEO0001 | Add one clear homepage H1 | Homepage H1 count = 1 | OperationsHandover |
| REC0007 | SEO0002 | Add unique homepage meta description | Non-empty meta description on `/` | OperationsHandover |
| REC0008 | SEO0003 | Implement Organization + Product JSON-LD | ld+json present on home and PDP | OperationsHandover |
| REC0009 | SEO0005 | Add homepage og:image | og:image present on `/` | OperationsHandover |
| REC0010 | P0001 | Rewrite refund for food/ghee; publish real return address | No INSERT; no apparel unworn language | OperationsHandover |
| REC0011 | P0002 | Publish stable HTTP 200 shipping policy | Shipping URL stable 200 | OperationsHandover |
| REC0012 | FUNC0004 | Point nav to live collection handles or remove bad links | Bad handles gone or redirected | OperationsHandover |
| REC0013 | FUNC0005 | Publish FAQ or remove FAQ references | FAQ 200 or zero FAQ hrefs | OperationsHandover |

## P1 recommendations (next)

| Rec ID | Issue ID | Recommendation | Owner report |
|--------|----------|----------------|--------------|
| REC0014 | SEO0004 | Unique meta descriptions on policy pages | Documentation / Seo |
| REC0015 | ACC0001 | Meaningful alt text on content images | Accessibility |
| REC0016 | PERF0001 | Enable srcset on home/PDP/collection | Performance |
| REC0017 | PERF0002 | Trim homepage sections/apps reducing HTML/JS weight | Performance |
| REC0018 | P0003 | Single NAP everywhere (footer = privacy = contact) | Documentation |
| REC0019 | UX0003 | Fix “Batch Teste” typo | UiReview |
| REC0020 | FUNC0006 | Remove Turmeric chip or add SKU | FunctionalTesting |
| REC0021 | ARCH0001 | Unpublish empty collections | Architecture |
| REC0022 | ARCH0002 | Consolidate overlapping collection indexes | Architecture |
| REC0023 | ARCH0003 | Publish blog posts or unpublish/noindex empty blog | Architecture |
| REC0024 | SEC0001 | Add Referrer-Policy | Security |
| REC0025 | SEC0002 | Add Permissions-Policy | Security |
| REC0026 | SEC0003 | Tighten CSP where platform allows | Security |
| REC0027 | P0004 | Publish or unlink unreachable ancillary policies | Documentation |
| REC0028 | ACC0002 | Single H1 on cart template | Accessibility |

## Evidence gap recommendations (documentation only)

| Rec ID | Evidence ID | Recommendation |
|--------|-------------|----------------|
| REC0029 | EV0017 | Capture annotated screenshots in a future pass |
| REC0030 | EV0018 | Run axe/WAVE and store export |
| REC0031 | EV0019 | Run Lighthouse/PSI and store report |
| REC0032 | EV0025-EV0027 | Staged human tests where scope allows |

## Mapping rule

Every recommendation above maps to an existing Issue ID or Evidence gap ID. Closing a recommendation requires new Evidence IDs and IssuesRegister status updates per [RepositoryLifecycle.md](./RepositoryLifecycle.md).

## Related

[IssuesRegister.md](./IssuesRegister.md) · [Reports/OperationsHandover.md](./Reports/OperationsHandover.md) · [RiskRegister.md](./RiskRegister.md)
