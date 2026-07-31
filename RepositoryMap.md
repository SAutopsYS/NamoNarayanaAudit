# Repository Map

Information architecture of `NamoNarayanaAudit/`.

```text
NamoNarayanaAudit/  (knowledge root)
  Core narrative and release docs
  Discovery/          (what exists on the site)
  Reports/            (discipline findings)
  Evidence/           (proof artifacts)
  Registers/          (IDs, issues, traceability)
  Standards/          (rules)
  Supporting knowledge docs  (this layer)
```


## Root

| Field | Detail |
|-------|--------|
| Purpose | Entry point for all audiences |
| Contents | README, AuditReport, EvidenceManifest, EvidenceIndex, DecisionLog, AuditTimeline, ReviewerGuide, RepositoryMap, NavigationIndex, RepositoryGlossary, RepositoryLifecycle, EvidenceGapRegister, RepositoryValidation, RepositoryReleaseChecklist, RepositoryStatistics, EvidenceCollectionGuide, Changelog, License |
| Dependencies | None (documents depend downward) |


## Reports/

| Field | Detail |
|-------|--------|
| Purpose | Domain-specific verified findings |
| Contents | 20 PascalCase reports (ProjectObjective … AuditClosure) |
| Dependencies | Discovery/AuditPlan · Registers/IssuesRegister · Evidence IDs |

```text
Reports/
  ↓ cite
IssuesRegister + EvidenceManifest
  ↓ roll up into
AuditReport / ExecutiveDashboard
```


## Evidence/

| Field | Detail |
|-------|--------|
| Purpose | Durable proof; never invent captures |
| Contents | Domain folders (Home, Products, Collections, Policies, Navigation, Checkout, Search, Accessibility, SEO, Security, Performance, Discovery, Headers, HTML, Screenshots, Reports) + Metadata/ |
| Dependencies | Capture process in EvidenceCollectionGuide |

```text
Evidence/<Domain>/file
  ↓
Metadata/EVnnnn.md (SHA256 if Exists)
  ↓
EvidenceManifest + EvidenceIndex
```


## Registers/

| Field | Detail |
|-------|--------|
| Purpose | System of record for defects and chains |
| Contents | IssueIdMap · IssuesRegister · TraceabilityMatrix |
| Dependencies | EvidenceManifest · DecisionLog (for severity/policy decisions) |


## Discovery/

| Field | Detail |
|-------|--------|
| Purpose | URL inventory and audit coverage plan |
| Contents | DiscoveredPages · PageInventory · AuditPlan |
| Dependencies | EV0001-EV0010 |


## Standards/

| Field | Detail |
|-------|--------|
| Purpose | Filename, ID, and report conventions |
| Contents | RepositoryStandards.md |
| Dependencies | Enforced by RepositoryValidation |


## Assets

| Field | Detail |
|-------|--------|
| Purpose | Binary/visual assets when collected |
| Contents | Intended under Evidence/Screenshots (currently Missing; EV0017) |
| Dependencies | Must register EV IDs before citation |

No fabricated PNG/JPEG assets are present.


## Supporting Documents (knowledge layer)

| Doc | Role |
|-----|------|
| DecisionLog | Why major calls were made |
| AuditTimeline | Chronology of stages |
| ReviewerGuide | Onboarding / 10-minute path |
| RepositoryMap | This IA view |
| EvidenceGapRegister | Missing/CBC evidence backlog |
| NavigationIndex | Clickable catalog |
| RepositoryGlossary | Terminology |
| RepositoryLifecycle | Maintenance playbook |

Dependencies: all point at frozen findings; they do not alter IssuesRegister severities.


## Dependency sketch

```text
Discovery -> AuditPlan -> Reports
Evidence and Registers feed AuditReport
DecisionLog / Timeline / Lifecycle support the release narrative
```

