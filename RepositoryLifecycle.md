# Repository Lifecycle

How to maintain WebsiteAudit/ after the Knowledge Base Release without corrupting the archive.


## Maintenance principles

1. Findings are immutable unless new dated evidence supports a change.  
2. PascalCase filenames only.  
3. Every new file gets an Evidence ID or is pure documentation (no fake “proof”).  
4. DecisionLog records methodology/readiness calls; IssuesRegister records defects.


## How future audits should be added

| Step | Action |
|------|--------|
| 1 | Create a dated branch or folder note in Changelog (for example `AuditWave-2026-Q4`) |
| 2 | Re-run discovery; store new CSV/JSON as **new** EV IDs (do not overwrite EV0001 bytes silently) |
| 3 | Diff against prior IssuesRegister |
| 4 | Update statuses; add new Issue IDs only for net-new defects |
| 5 | Refresh RemediationValidation, AuditReport verdict section, DecisionLog if readiness changes |
| 6 | Run RepositoryValidation + update RepositoryStatistics |

Prefer appending evidence over mutating historical baselines. Baselines (EV0001, EV0011, EV0014, EV0016) stay as the 2026-07-30 snapshot.


## Versioning strategy

| Layer | Approach |
|-------|----------|
| Documentation | Changelog semantic sections (Added/Changed/Not changed) |
| Evidence | Monotonic EV IDs; SHA256 sidecars |
| Issues | Permanent IDs; status field changes over time |
| Decisions | New DECnnnn; mark old decisions Superseded if replaced |
| Git | Tag releases `kb-release-2026-07-30`, `revalidation-YYYY-MM-DD` |


## Evidence update process

Follow [EvidenceCollectionGuide.md](./EvidenceCollectionGuide.md):

1. Store file in correct Evidence/ domain folder.  
2. Write Metadata/EVnnnn.md with SHA256.  
3. Update EvidenceManifest + EvidenceIndex (+ Gap Register if closing a gap).  
4. Cite the new ID from Issues/Reports.  
5. Never invent screenshots or lab scores.


## Issue closure workflow

```text
Remediate live site
  → Capture new evidence (new EV ID)
  → Update IssuesRegister status to Fixed
  → Update RemediationValidation table
  → Recompute ProductionGovernance gates
  → If paid-ads readiness changes, add DecisionLog entry
  → Changelog
```

Closing an issue **without** new evidence is forbidden.


## Repository review workflow

| Cadence | Review |
|---------|--------|
| After every remediation claim | RemediationValidation + EV IDs |
| Quarterly | Discovery re-crawl sample; link rot check |
| Before external publish | RepositoryReleaseChecklist + Validation |
| Onboarding new reviewers | ReviewerGuide 10-minute path |


## Archiving process

1. Freeze a git tag.  
2. Export AuditReport (+ optional PDF) for client packet.  
3. Retain Evidence/Metadata hashes.  
4. Leave legacy `website-audit/` untouched as historical non-canonical copy (DEC0012).  
5. Record archive event in Changelog.


## Roles

| Role | Owns |
|------|------|
| QA Lead | Issue severity policy, validation |
| Evidence Engineer | EV IDs, hashes, gaps |
| Documentation Engineer | Reports, knowledge docs, links |
| Release Manager | Checklist, tags, GitHub publish |
| Client Operator | Live remediation execution |


## Related

[DecisionLog.md](./DecisionLog.md) · [ReviewerGuide.md](./ReviewerGuide.md) · [Standards/RepositoryStandards.md](./Standards/RepositoryStandards.md) · [RepositoryValidation.md](./RepositoryValidation.md)

