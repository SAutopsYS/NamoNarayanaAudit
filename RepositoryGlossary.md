# Repository Glossary

Terms used across WebsiteAudit/. Definitions match how this archive applies them.

| Term | Meaning here |
|------|----------------|
| **Accessibility** | Observable public HTML barriers (headings, alt text). Full WCAG certification not claimed without tooling (EV0018 Missing). |
| **Audit Closure** | End of documentation engagement; separate from site readiness. |
| **Audit Timeline** | Chronological stages from discovery through knowledge release. |
| **Business Impact** | Qualitative risk/opportunity from verified defects; no invented ROI. |
| **Cannot Be Collected** | Evidence status: blocked by scope/policy/technical abort this engagement. |
| **Conditional Certification** | Docs certified complete for public scope; storefront not certified for paid launch (DEC0004). |
| **Core Web Vitals** | Field/lab performance metrics. Not scored here (NV0001 / EV0019 Missing). |
| **Decision ID** | `DECnnnn` entry in DecisionLog recording a governance or methodology call. |
| **Discovery** | Enumeration of public URLs before reporting; inventory is authoritative. |
| **Evidence** | Retained artifact (CSV, XML, JSONL, notes, etc.) cited by Evidence ID. |
| **Evidence Exists** | File on disk with Metadata SHA256. |
| **Evidence Gap** | Missing or Cannot Be Collected item tracked in EvidenceGapRegister. |
| **Evidence ID** | Permanent `EVnnnn` identifier for an evidence record. |
| **Evidence Missing** | Not captured yet; collectable later without inventing files. |
| **Governance** | Publish gates and ID/severity control (ProductionGovernance, DecisionLog). |
| **Issue ID** | Permanent defect ID with domain prefix (`FUNC0001`, `SEO0001`, `P0001`, …). |
| **Knowledge Base Release** | Repository state optimized for onboarding and archive (DEC0010). |
| **P0** | Highest severity: blocks trust, legal completeness, or primary-landing foundations. |
| **P1** | High severity: material quality/hardening/IA debt; not the first launch gate alone. |
| **Paid Ads Not Ready** | Decision DEC0003: do not scale paid traffic until P0 Fixed with new evidence. |
| **Release Candidate** | Documentation package approved for GitHub/client/portfolio delivery (DEC0009). |
| **Remediation Validation** | Retest ledger proving whether Issues flipped to Fixed. |
| **Repository Hardening** | Phase 21: PascalCase structure, permanent IDs, Evidence tree. |
| **Structured Data** | Machine-readable JSON-LD (Product/Organization). Absent on samples (SEO0003). |
| **Traceability** | Chain Issue → Evidence → Report → Recommendation → Status → Conclusion. |
| **Validation** | Confirmation against evidence; not a new discovery crawl by default. |
| **Working Control** | `CTRLnnnn` positive check that is working (not a defect). |
| **Not Verifiable (NV)** | `NVnnnn` item that public probes could not confirm. |

Related: [IssueIdMap.md](./Registers/IssueIdMap.md) · [EvidenceManifest.md](./EvidenceManifest.md) · [DecisionLog.md](./DecisionLog.md)

