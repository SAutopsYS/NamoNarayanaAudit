# Decision Log

Major decisions that shaped this audit archive. Decisions do not invent new findings; they record how existing evidence was interpreted and how the repository was governed.

**Owner role:** Audit / Documentation lead (public engagement)  
**Status values:** Active · Superseded · Historical


### DEC0001: Discovery before reporting
| Field | Value |
|-------|-------|
| Decision | No phase report may invent URLs; discovery inventory is authoritative |
| Reason | Prevents assumed pages (for example FAQ) that are absent from `pages.json` |
| Supporting Evidence IDs | EV0001, EV0002, EV0003 |
| Supporting Issue IDs | FUNC0005 (FAQ absence confirmed via discovery) |
| Supporting Reports | DiscoveredPages, AuditPlan, WebsiteDiscovery |
| Decision Date | 2026-07-30 |
| Decision Owner | Audit lead |
| Decision Status | Active |

### DEC0002: P0 classification criteria
| Field | Value |
|-------|-------|
| Decision | Defects that block trust, legal completeness, or primary-landing SEO/a11y foundations are P0 |
| Reason | Paid traffic and consumer trust fail first on homepage/policy integrity, not on secondary polish |
| Supporting Evidence IDs | EV0014, EV0016, EV0001 |
| Supporting Issue IDs | FUNC0001-FUNC0005, UX0001-UX0002, SEO0001-SEO0003, P0001-P0002 |
| Supporting Reports | IssuesRegister, ProductionGovernance, BusinessImpact |
| Decision Date | 2026-07-30 |
| Decision Owner | QA governance lead |
| Decision Status | Active |

### DEC0003: Paid ads not ready
| Field | Value |
|-------|-------|
| Decision | Do not scale paid acquisition until P0 Issues are Fixed with new evidence |
| Reason | Homepage trust/SEO failures plus refund/shipping gaps create brand and compliance risk |
| Supporting Evidence IDs | EV0014, EV0016, EV0001 |
| Supporting Issue IDs | All open P0 IDs (12) |
| Supporting Reports | AuditReport, BusinessImpact, ExecutiveDashboard |
| Decision Date | 2026-07-30 |
| Decision Owner | Audit lead |
| Decision Status | Active |

### DEC0004: Conditional certification of documentation only
| Field | Value |
|-------|-------|
| Decision | Certify the audit package as complete for public-access scope; do not certify the live storefront for paid launch |
| Reason | Documentation completeness ≠ production readiness; 0 P0 Fixed |
| Supporting Evidence IDs | EV0001, EvidenceManifest Exists set |
| Supporting Issue IDs | P0 open set |
| Supporting Reports | AuditClosure, RepositoryValidation, AuditReport |
| Decision Date | 2026-07-30 |
| Decision Owner | Audit lead |
| Decision Status | Active |

### DEC0005: Permanent Issue ID scheme
| Field | Value |
|-------|-------|
| Decision | Replace working `NN-###` IDs with domain-prefixed permanent IDs (`FUNC`, `SEO`, `P`, …) |
| Reason | Stable remediation tracking across repository hardening and future audits |
| Supporting Evidence IDs |; (governance decision) |
| Supporting Issue IDs | All mapped IDs in IssueIdMap |
| Supporting Reports | IssueIdMap, IssuesRegister, TraceabilityMatrix |
| Decision Date | 2026-07-30 |
| Decision Owner | Documentation architect |
| Decision Status | Active |

### DEC0006: No fabricated lab or visual evidence
| Field | Value |
|-------|-------|
| Decision | Screenshots, Lighthouse, and axe/WAVE exports are Missing or out of scope; never invented |
| Reason | Enterprise archive integrity; false captures destroy trust |
| Supporting Evidence IDs | EV0017-EV0020, EV0025-EV0027 |
| Supporting Issue IDs | NV0001-NV0006 |
| Supporting Reports | EvidenceManifest, EvidenceGapRegister, EvidenceCollectionGuide |
| Decision Date | 2026-07-30 |
| Decision Owner | Evidence engineer |
| Decision Status | Active |

### DEC0007: One Issue ID per defect (no duplicate cross-domain IDs)
| Field | Value |
|-------|-------|
| Decision | Homepage missing H1 remains SEO0001; accessibility impact is cited in Accessibility report without a second ID |
| Reason | Prevent double-counting and conflicting statuses |
| Supporting Evidence IDs | EV0014 |
| Supporting Issue IDs | SEO0001, ACC0001, ACC0002 |
| Supporting Reports | IssueIdMap, Accessibility, Seo |
| Decision Date | 2026-07-30 |
| Decision Owner | QA governance lead |
| Decision Status | Active |

### DEC0008: Public probe scope excludes payment completion
| Field | Value |
|-------|-------|
| Decision | Checkout entry is verified; payment authorization is Not Verifiable / Cannot Be Collected |
| Reason | Platform/agent policy requires buyer approval for payment; not in engagement scope |
| Supporting Evidence IDs | EV0021, EV0026 |
| Supporting Issue IDs | CTRL0006, NV0005 |
| Supporting Reports | FunctionalTesting, Security |
| Decision Date | 2026-07-30 |
| Decision Owner | Audit lead |
| Decision Status | Active |

### DEC0009: Repository release candidate (documentation)
| Field | Value |
|-------|-------|
| Decision | Approve WebsiteAudit/ as release candidate for GitHub, client delivery, and portfolio |
| Reason | Structure, IDs, evidence classification, and knowledge layer meet delivery bar; site readiness remains fail |
| Supporting Evidence IDs | Exists set EV0001-EV0016, EV0021-EV0024 |
| Supporting Issue IDs | N/A |
| Supporting Reports | RepositoryReleaseChecklist, RepositoryValidation, RepositoryStatistics |
| Decision Date | 2026-07-30 |
| Decision Owner | Repository release manager |
| Decision Status | Active |

### DEC0010: Knowledge Base Release (this layer)
| Field | Value |
|-------|-------|
| Decision | Add DecisionLog, Timeline, ReviewerGuide, Map, Gap Register, Navigation, Glossary, Lifecycle without changing findings |
| Reason | Improve discoverability and long-term maintainability for enterprise archive use |
| Supporting Evidence IDs |; (documentation governance) |
| Supporting Issue IDs | N/A |
| Supporting Reports | ReviewerGuide, RepositoryMap, NavigationIndex |
| Decision Date | 2026-07-30 |
| Decision Owner | Knowledge architect |
| Decision Status | Active |

### DEC0011: Governance gate score 4/17 PASS
| Field | Value |
|-------|-------|
| Decision | Production publish gates remain 4/17 PASS based on explicit gate table |
| Reason | Only transport/robots/search/checkout-class controls pass; P0 content/policy gates fail |
| Supporting Evidence IDs | EV0001, EV0013, EV0014 |
| Supporting Issue IDs | FAIL-linked P0/P1 set in ProductionGovernance |
| Supporting Reports | ProductionGovernance, ExecutiveDashboard |
| Decision Date | 2026-07-30 |
| Decision Owner | QA governance lead |
| Decision Status | Active |

### DEC0012: Legacy website-audit/ is non-canonical
| Field | Value |
|-------|-------|
| Decision | Hyphenated `website-audit/` retained as historical working copy; WebsiteAudit/ is delivery root |
| Reason | PascalCase enterprise structure is the maintained knowledge base |
| Supporting Evidence IDs | N/A |
| Supporting Issue IDs | N/A |
| Supporting Reports | Changelog, README |
| Decision Date | 2026-07-30 |
| Decision Owner | Repository strategist |
| Decision Status | Active |


## How to add a decision

1. Assign next `DECnnnn`.  
2. Link Evidence / Issue / Report IDs that already exist.  
3. Do not use DecisionLog to create new defects.  
4. Update Changelog.

