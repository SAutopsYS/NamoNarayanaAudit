# Audit Timeline

Chronological history of the Namo Narayana public audit and repository build.  
**Website:** https://namonarayana.com/  
**Primary evidence date:** 2026-07-30


## 1. Discovery

| Field | Detail |
|-------|--------|
| Purpose | Enumerate every public URL before reporting |
| Input | robots.txt, sitemap index/children, Shopify JSON APIs, seeded paths |
| Output | 60 probed URLs; reachability and indexability |
| Deliverables | EV0001-EV0010 · Discovery/DiscoveredPages.md · PageInventory.md |

## 2. Planning

| Field | Detail |
|-------|--------|
| Purpose | Bind each report to required templates only |
| Input | Discovery inventory |
| Output | Coverage matrix (which report owns which URLs) |
| Deliverables | Discovery/AuditPlan.md |

## 3. Research

| Field | Detail |
|-------|--------|
| Purpose | Capture brand/NAP/public entity signals |
| Input | About, story, contact, privacy pages from inventory |
| Output | Company context; NAP conflict recorded as P0003 |
| Deliverables | Reports/CompanyResearch.md |

## 4. Testing

| Field | Detail |
|-------|--------|
| Purpose | Functional, UI, UX, a11y, SEO, security, performance probes on planned templates |
| Input | AuditPlan minimum URL set |
| Output | TemplateEvidence.jsonl metrics; issue candidates |
| Deliverables | EV0011-EV0016, EV0021-EV0024 · Reports 04-13 equivalents |

## 5. Validation

| Field | Detail |
|-------|--------|
| Purpose | Retest ledger against prior P0 hypotheses using frozen evidence |
| Input | IssuesRegister + EV0011/EV0014/EV0016 |
| Output | 0 P0 Fixed confirmed |
| Deliverables | Reports/RemediationValidation.md |

## 6. Governance

| Field | Detail |
|-------|--------|
| Purpose | Define publish gates and permanent Issue IDs |
| Input | Open issues + working controls |
| Output | 4/17 PASS gate score; IssueIdMap |
| Deliverables | ProductionGovernance.md · IssueIdMap.md · DEC0002, DEC0005, DEC0011 |

## 7. Business Review

| Field | Detail |
|-------|--------|
| Purpose | Translate defects to qualitative business risk (no invented ROI) |
| Input | P0/P1 register + sellable SKU set |
| Output | Paid-ads Not Ready recommendation |
| Deliverables | BusinessImpact.md · ExecutiveDashboard.md · DEC0003 |

## 8. Operations Handover

| Field | Detail |
|-------|--------|
| Purpose | Ordered fix sequence with acceptance tests |
| Input | P0 list |
| Output | Ten-step remediation runbook |
| Deliverables | OperationsHandover.md |

## 9. Audit Closure

| Field | Detail |
|-------|--------|
| Purpose | Close documentation engagement; state certifications clearly |
| Input | Full package |
| Output | Docs certified complete; site not certified for paid launch |
| Deliverables | AuditClosure.md · AuditReport.md · DEC0004 |

## 10. Repository Hardening (Phase 21)

| Field | Detail |
|-------|--------|
| Purpose | PascalCase enterprise structure, permanent IDs, Evidence tree |
| Input | Working `website-audit/` package |
| Output | Canonical WebsiteAudit/ |
| Deliverables | README · Registers · Reports · Evidence folders · DEC0009, DEC0012 |

## 11. Evidence Collection (Phase 22)

| Field | Detail |
|-------|--------|
| Purpose | Classify Exists / Missing / Cannot Be Collected; SHA256 metadata |
| Input | Existing files only |
| Output | Manifest classification; Metadata sidecars |
| Deliverables | EvidenceManifest · EvidenceIndex · EvidenceCollectionGuide · DEC0006 |

## 12. Repository Release / Knowledge Layer

| Field | Detail |
|-------|--------|
| Purpose | Self-explanatory knowledge base for onboarding and archive |
| Input | Hardened + evidence-backed repo |
| Output | Knowledge Base Release docs |
| Deliverables | DecisionLog · AuditTimeline · ReviewerGuide · RepositoryMap · EvidenceGapRegister · NavigationIndex · RepositoryGlossary · RepositoryLifecycle · DEC0010 |


## Timeline at a glance

```text
Discovery → Plan → Research → Testing → Validation
    → Governance → Business → Ops Handover → Closure
    → Harden → Evidence → Knowledge Release
```

All stages share the same evidence date unless a future re-audit adds new EV IDs.

