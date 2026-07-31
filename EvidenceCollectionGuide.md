# Evidence Collection Guide

## Purpose

Define how evidence in `WebsiteAudit/` was gathered, how to add more, and what must never be fabricated.

## How evidence was collected

| Phase | Method | Output |
|-------|--------|--------|
| Discovery | `Invoke-WebRequest` against sitemaps, robots.txt, Shopify JSON APIs, seeded URLs | EV0001-EV0010 |
| Template probes | PowerShell batch parse of HTML/headers for critical templates | EV0011 / EV0012 |
| Derived notes | Extracts from EV0011 / EV0001 without new live calls during Phase 21-22 | EV0013-EV0016, EV0021-EV0024 |
| Phase 22 | Classification, SHA256 metadata, folder organization | Evidence/Metadata/* |

No browser screenshot automation. No Lighthouse CI. No axe/WAVE CLI dump.

## Allowed evidence types

PNG · JPEG · HTML · PDF · TXT · JSON · JSONL · HAR · CSV · XML · Response header summaries · Page source · robots.txt · sitemap.xml · Markdown probe notes derived from verified captures

## Naming standards

- Repository paths and documentation: **PascalCase** (`HomeProbeNotes.md`, `DiscoveredPages.csv`)
- Evidence IDs: `EVnnnn` (zero-padded)
- Issue IDs: domain prefix + four digits (`FUNC0001`)
- Never invent filenames that imply captures not performed (for example `Homepage.png` without a real file)

## Folder conventions

```
Evidence/
  Home|Products|Collections|Policies|Navigation|Checkout|Search|
  Accessibility|SEO|Security|Performance|Discovery|Headers|HTML|
  Screenshots|Reports|Metadata/
```

Each domain folder has `README.md` describing purpose and related reports.

## Verification process

1. Place file in the correct domain folder.  
2. Compute SHA256 (`Get-FileHash -Algorithm SHA256`).  
3. Create `Evidence/Metadata/EVnnnn.md` with required fields.  
4. Add/update row in `EvidenceManifest.md` with availability status.  
5. Update `EvidenceIndex.md` grouping.  
6. Cite the Evidence ID from IssuesRegister / reports.  
7. Refresh `RepositoryStatistics.md` counts.

## Availability statuses

| Status | When to use |
|--------|-------------|
| Evidence Exists | Bytes on disk + metadata + SHA256 |
| Evidence Missing | Collectable later; not present now |
| Evidence Cannot Be Collected | Blocked by scope, policy, or technical abort |

## Citation format

```markdown
### Evidence
- **EV0014**: Homepage metrics  
  See: `Evidence/Home/HomeProbeNotes.md`  
  Metadata: `Evidence/Metadata/EV0014.md`
```

Prefer IDs over bare filenames in report bodies.

## Limitations

- Public HTTP only; no admin session captures.  
- Some URLs aborted before HTTP status bodies (EV0027 / NV0006).  
- Screenshots, Lighthouse, and axe exports remain Missing (EV0017-EV0019).  
- Payment and form-delivery proof Cannot Be Collected this engagement (EV0025-EV0026).  
- Derived Markdown notes are secondary; machine source of truth for metrics is EV0011.

## Prohibited actions

- Inventing screenshots or lab scores  
- Changing Issue severity to “match” missing evidence  
- Committing secrets, card data, or customer PII  
- Citing a path that does not exist on disk

