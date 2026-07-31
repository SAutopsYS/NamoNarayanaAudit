# Traceability Matrix

## Purpose

Prove every Issue ID links Evidence → Report → Recommendation → Status → Audit conclusion with no orphans.

Related knowledge docs: [DecisionLog.md](./DecisionLog.md) · [EvidenceGapRegister.md](./EvidenceGapRegister.md) · [ReviewerGuide.md](./ReviewerGuide.md) · [AuditReport.md](./AuditReport.md)

## Chain

```
Evidence (EVnnnn)
    ↓
Report (Reports/*.md)
    ↓
Recommendation (IssuesRegister + report)
    ↓
Final Status (IssuesRegister)
    ↓
Audit Conclusion (AuditReport.md / AuditClosure.md)
```

## Issue traceability

| Issue ID | Evidence | Primary Report | Recommendation owner | Status | Conclusion anchor |
|----------|----------|----------------|----------------------|--------|-------------------|
| FUNC0001 | EV0012/EV0014 | FunctionalTesting, UiReview | OperationsHandover step 1 | ❌ Still Exists | AuditReport Risk Summary |
| UX0001 | EV0012/EV0014 | UxReview | OperationsHandover step 3 | ❌ Still Exists | AuditReport |
| UX0002 | EV0012/EV0014 | UxReview, Seo | OperationsHandover step 3 | ❌ Still Exists | AuditReport |
| SEO0001 | EV0012/EV0014 | Seo, Accessibility | OperationsHandover step 7 | ❌ Still Exists | AuditReport |
| SEO0002 | EV0012/EV0014 | Seo | OperationsHandover step 7 | ❌ Still Exists | AuditReport |
| SEO0003 | EV0012 | Seo, Architecture | OperationsHandover step 8 | ❌ Still Exists | AuditReport |
| P0001 | EV0016 | Documentation, FunctionalTesting | OperationsHandover step 4 | ❌ Still Exists | AuditReport |
| P0002 | EV0001, EV0012 | Documentation, FunctionalTesting | OperationsHandover step 5 | ❌ Still Exists | AuditReport |
| FUNC0002 | EV0012/EV0014 | UiReview, Performance | OperationsHandover step 2 | ❌ Still Exists | AuditReport |
| FUNC0003 | EV0012, EV0001 | FunctionalTesting, Architecture | OperationsHandover step 2 | ❌ Still Exists | AuditReport |
| FUNC0004 | EV0001, EV0023 | FunctionalTesting, Architecture | OperationsHandover step 9 | ❌ Still Exists | AuditReport |
| FUNC0005 | EV0001, EV0012 | FunctionalTesting, Documentation | OperationsHandover step 6 | ❌ Still Exists | AuditReport |
| SEO0004 | EV0012 | Seo, Documentation | Documentation recommendations | ❌ Still Exists | AuditReport |
| ACC0001 | EV0012/EV0014/EV0015 | Accessibility | Accessibility recommendations | ❌ Still Exists | AuditReport |
| PERF0001 | EV0012 | Performance, ResponsiveTesting | Performance recommendations | ❌ Still Exists | AuditReport |
| PERF0002 | EV0012/EV0014 | Performance | Performance recommendations | ❌ Still Exists | AuditReport |
| SEO0005 | EV0012/EV0014 | Seo | OperationsHandover step 7 | ❌ Still Exists | AuditReport |
| P0003 | EV0012 | CompanyResearch, Documentation | OperationsHandover step 10 | ❌ Still Exists | AuditReport |
| UX0003 | EV0012 | UiReview | UiReview recommendations | ❌ Still Exists | AuditReport |
| FUNC0006 | EV0012 | FunctionalTesting | FunctionalTesting recommendations | ❌ Still Exists | AuditReport |
| ARCH0001 | EV0001, EV0022 | Architecture | ProductionGovernance gate 13 | ❌ Still Exists | AuditReport |
| ARCH0002 | EV0001, EV0022 | Architecture, Seo | Architecture recommendations | ❌ Still Exists | AuditReport |
| SEC0001 | EV0013 | Security | Security recommendations | ❌ Still Exists | AuditReport |
| SEC0002 | EV0013 | Security | Security recommendations | ❌ Still Exists | AuditReport |
| SEC0003 | EV0013 | Security | Security recommendations | ❌ Still Exists | AuditReport |
| P0004 | EV0001 | Documentation | Documentation recommendations | ❌ Still Exists | AuditReport |
| ARCH0003 | EV0001, EV0009 | Architecture, Seo | Architecture recommendations | ❌ Still Exists | AuditReport |
| ACC0002 | EV0012 | Accessibility, UiReview | UiReview/Accessibility | ❌ Still Exists | AuditReport |

## Controls and NV items

| ID | Evidence | Report | Status |
|----|----------|--------|--------|
| CTRL0001-CTRL0012 | EV0001, EV0011, EV0013 | FunctionalTesting, Security, Seo | ✅ Working |
| NV0001-NV0006 | Manifest rows EV0017-EV0019 where applicable | Accessibility, Performance, FunctionalTesting | ⚪ Not Verifiable / Evidence Not Yet Collected |

## Orphan check

| Check | Result |
|-------|--------|
| Issue without evidence | None |
| Issue without report | None |
| Evidence without manifest row | None for Verified files |
| Screenshot evidence claimed | No; EV0017 marked Not Yet Collected |

## Conclusion

Traceability is complete for the hardened repository.

