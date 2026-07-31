# Changelog

All notable changes to the Namo Narayana audit documentation release.

## [2026-07-31]: Final formatting standard

### Changed

- Removed decorative em dashes, en-dash dividers, and repeated-dash horizontal rules from all Markdown across `NamoNarayanaAudit/`, `WebsiteAudit/`, and `website-audit/`
- Replaced section dividers with headings, spacing, tables, and lists
- Left raw evidence captures (robots.txt, JSON probes) unchanged

### Not changed

- Website findings, severities, statuses, and paid-ads verdict

## [2026-07-30]: Release Acceptance PASS (v1.0.0)

### Added

- `ReleaseAcceptance.md`: acceptance criteria record (**PASS**)

### Changed

- Cleared residual `TBD` wording in Evidence READMEs / EvidenceIndex

## [2026-07-30]: Final Release (NamoNarayanaAudit)

### Added

- Final delivery folder `NamoNarayanaAudit/`
- `STARTHERE.md`, `ExecutiveSummary.md`
- `RecommendationsRegister.md`, `RiskRegister.md`
- `Assets/` notice folder
- Release README with website overview and health dashboard

### Changed

- PascalCase `ChangeLog.md`
- Removed decorative `---` horizontal rules from Markdown
- Root copies of IssuesRegister and TraceabilityMatrix with corrected links

### Not changed

- Website audit findings, severities, and paid-ads verdict

## Historical notes (WebsiteAudit working package)

The entries below record documentation work that originated in the WebsiteAudit working package before the final NamoNarayanaAudit release folder.

## [2026-07-30]: Repository QA Review

### Added

- `RepositoryQAReview.md`: independent documentation QA of WebsiteAudit/
- NavigationIndex entry for RepositoryQAReview

### Review outcome

- Verdict: **Needs Minor Documentation Updates** (mean quality score 8.7/10)
- Website audit findings/severities/conclusions: unchanged
- Action items QA-A1-A7 recorded in RepositoryQAReview (not auto-applied except nav/changelog indexing)

## [2026-07-30]: Knowledge Base Release

### Added

- `DecisionLog.md` (DEC0001-DEC0012)
- `AuditTimeline.md`
- `ReviewerGuide.md`
- `RepositoryMap.md`
- `EvidenceGapRegister.md`
- `NavigationIndex.md`
- `RepositoryGlossary.md`
- `RepositoryLifecycle.md`

### Changed

- README and AuditReport cross-links to knowledge layer
- RepositoryValidation usability review section
- IssuesRegister / TraceabilityMatrix / EvidenceManifest pointers

### Not changed

- Findings, severities, P0 statuses, paid-ads verdict

## [2026-07-30]: Phase 22 Evidence Collection

### Added

- Evidence availability classification: Exists / Missing / Cannot Be Collected
- `Evidence/Metadata/EVnnnn.md` sidecars with SHA256 for all Exists artifacts
- Evidence IDs EV0021-EV0024 for previously unlisted note files
- Evidence IDs EV0025-EV0027 for Cannot Be Collected scope limits
- `EvidenceIndex.md`, `EvidenceCollectionGuide.md`
- `RepositoryReleaseChecklist.md`, `RepositoryStatistics.md`
- Screenshots `MissingEvidenceNotice.md` (no fabricated images)

### Changed

- `EvidenceManifest.md` rewritten with availability statuses
- All 20 reports’ Evidence References now cite Evidence IDs + See paths
- `RepositoryValidation.md` updated for Phase 22 orphan/gap documentation
- README navigation entries for evidence release docs

### Not changed

- Issue severities, statuses, or audit conclusions
- No new live website audit
- No invented screenshots or Lighthouse/axe files

## [2026-07-30]: Phase 21 Repository Hardening

### Added

- Canonical enterprise root `WebsiteAudit/`
- Permanent Issue IDs (`FUNC`, `SEO`, `SEC`, `UX`, `ACC`, `PERF`, `ARCH`, `P`)
- `Registers/IssueIdMap.md` mapping legacy `NN-###` → permanent IDs
- `EvidenceManifest.md` with EV0001-EV0020
- `Evidence/` domain tree with README.md in each folder
- Derived probe notes (Home, PDP, Refund, Headers, Navigation, Search, Collections, Checkout)
- `AuditReport.md` client/recruiter master document
- `RepositoryValidation.md`
- `Standards/RepositoryStandards.md`
- PascalCase `Reports/*` (20) and `Discovery/*` (3)

### Changed

- README rewritten as project dashboard
- Reports standardized to Purpose → Conclusion sections
- Traceability rewritten around Evidence → Report → Recommendation → Status → Conclusion
- Terminology normalized to permanent Issue IDs

### Not changed

- Issue severities
- Open/Fixed statuses (still 0 P0 Fixed)
- Audit conclusions (Not ready for paid ads)
- No new live website findings invented

### Historical note

Working package `website-audit/` (hyphenated) remains as pre-hardening source material. **WebsiteAudit/** is the delivery canonical.

