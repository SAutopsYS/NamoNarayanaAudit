# Audit Plan

## Purpose

Map each report to the minimum verified page set required for that discipline. Prevents duplicate narrative and unscoped probing.

## Scope

All reports under `Reports/` plus discovery and register documents.

## Methodology

Template classes defined from EV0001. Each report lists only the classes it owns.

## Verified Findings (coverage matrix)

| Report | Required templates / URLs |
|--------|---------------------------|
| ProjectObjective | Discovery docs only |
| CompanyResearch | Home, about-us, our-story, contact, privacy |
| WebsiteDiscovery | Inventory summary (points to Discovery/) |
| FunctionalTesting | SearchÃ: 3, cart, checkout entry, live PDP, contact, refund, shipping, FAQ, broken collections |
| UiReview | Home, ghee collection, empty collection, live PDP, zero-price PDP, contact, cart |
| ResponsiveTesting | Home, live PDP, collection, cart, search |
| UxReview | Funnel: home â†’ collection â†’ PDP â†’ cart â†’ checkout + policies |
| Accessibility | One URL per HTML template class |
| Performance | Home, live PDP, all-products |
| Seo | All indexable HTML + robots/sitemaps |
| Security | Headers on home, PDP, cart; checkout/login redirect observation |
| Architecture | Inventory duplicates/empties/global chrome |
| Documentation | Policies, pages, blog |
| ExecutiveDashboard | IssuesRegister aggregates |
| PortfolioCaseStudy | Narrative from registers |
| RemediationValidation | Prior P0 URL set |
| ProductionGovernance | Gate table from IssuesRegister |
| BusinessImpact | Sellable SKUs + P0 trust/legal set |
| OperationsHandover | Fix sequence from IssuesRegister |
| AuditClosure | Package completeness |

## Evidence References

EV0001, EV0003, EV0011

## Risk Analysis

Auditing without this plan reintroduces assumed pages (for example FAQ) that are not in `pages.json`.

## Business Impact

Scoped evidence keeps client delivery defensible.

## Recommendations

Update this matrix when new templates are published.

## Related Issues

:  (planning artifact)

## Related Evidence

EV0001, EV0003

## Related Reports

All `Reports/*`

## Conclusion

Phase reporting is bound to discovered URLs only.
