# Reviewer Guide

How to understand this repository in about ten minutes, then go deep by role.


## Where to start

Begin at [STARTHERE.md](./STARTHERE.md) or [ExecutiveSummary.md](./ExecutiveSummary.md).


| Your role | Open first | Then |
|-----------|------------|------|
| Client / leadership | [AuditReport.md](./AuditReport.md) | IssuesRegister → OperationsHandover |
| Recruiter / portfolio | [AuditReport.md](./AuditReport.md) | AuditTimeline → PortfolioCaseStudy |
| Engineer | [OperationsHandover.md](./Reports/OperationsHandover.md) | IssuesRegister → Evidence IDs |
| QA lead | [AuditTimeline.md](./AuditTimeline.md) | AuditPlan → EvidenceCollectionGuide |
| New teammate | [NavigationIndex.md](./NavigationIndex.md) | RepositoryMap → Glossary |

**10-minute path:** AuditReport (3 min) → DecisionLog DEC0003/DEC0004 (2 min) → IssuesRegister P0 table (3 min) → EvidenceIndex Home/Policies (2 min).


## How to read the repository

1. **Verdict first**: AuditReport Final Conclusion.  
2. **Decisions second**: why that verdict exists (DecisionLog).  
3. **Defects third**: IssuesRegister permanent IDs.  
4. **Proof fourth**: EvidenceManifest / EvidenceIndex.  
5. **Depth last**: domain Reports/ as needed.

Do not start in random report files; context lives at the root.


## How reports relate

- **Discovery/** defines what URLs exist.  
- **AuditPlan** assigns URLs to reports.  
- **Reports/** each own one discipline; they cite Issue IDs instead of copying full register rows.  
- **Registers/** are the system of record for defects and traceability.  
- **AuditReport** rolls up for external readers.


## How evidence is organised

```text
Evidence ID (EVnnnn)
  → folder under Evidence/<Domain>/
  → Metadata/EVnnnn.md (SHA256 when Exists)
  → cited from Issues + Reports
```

Statuses: **Exists** · **Missing** · **Cannot Be Collected**: see EvidenceGapRegister for gaps.


## How issue tracking works

- Permanent IDs: `FUNC`, `SEO`, `SEC`, `UX`, `ACC`, `PERF`, `ARCH`, `P`  
- Map from legacy `NN-###`: IssueIdMap  
- Status flips only after new dated Evidence IDs (Lifecycle)


## How traceability works

```text
Issue → Evidence → Report → Recommendation → Status → AuditReport conclusion
```

Full matrix: [Registers/TraceabilityMatrix.md](./Registers/TraceabilityMatrix.md)


## How conclusions were reached

| Conclusion | Decision | Basis |
|------------|----------|-------|
| Paid ads not ready | DEC0003 | 12 open P0; EV0014/EV0016/EV0001 |
| Docs complete / site not certified | DEC0004 | Package vs P0 Fixed = 0 |
| Release candidate for GitHub | DEC0009 | Structure + evidence classification |

No Lighthouse or axe scores were invented to support conclusions.


## How recommendations should be implemented

1. Follow [Reports/OperationsHandover.md](./Reports/OperationsHandover.md) steps 1-10.  
2. Re-probe; store new files; mint new EV IDs.  
3. Update IssuesRegister status + RemediationValidation.  
4. Re-check ProductionGovernance gates.  
5. Log decision if readiness changes (new DECnnnn).


## Frequently Asked Questions

**Q: Why are there no screenshots?**  
A: Not captured (EV0017 Missing). Metrics live in EV0011/EV0014. Do not fabricate images.

**Q: Is the site broken for buying ghee?**  
A: Checkout entry works for three live SKUs (CTRL0006/CTRL0007). Trust/policy layer is not launch-ready.

**Q: What is `website-audit/`?**  
A: Legacy working copy (DEC0012). Use WebsiteAudit/.

**Q: Can I change a P0 to P1?**  
A: Not without new verified evidence and a DecisionLog entry. Severity is frozen otherwise.

**Q: Where is the single client PDF equivalent?**  
A: AuditReport.md is the master narrative; export to PDF if needed for delivery.


## Repository navigation path

```text
README → AuditReport → DecisionLog → IssuesRegister
  → EvidenceIndex → OperationsHandover → RemediationValidation
  → RepositoryLifecycle (for maintainers)
```

Visual map: [RepositoryMap.md](./RepositoryMap.md)  
Clickable index: [NavigationIndex.md](./NavigationIndex.md)

