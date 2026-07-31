# Repository Standards

## Filenames

- Use **PascalCase** only: `FunctionalTesting.md`, `EvidenceManifest.md`
- Never use hyphens or spaces in filenames
- Acronyms may appear as full Pascal tokens: `Seo.md`, `UiReview.md`

## Issue IDs

- Permanent domain prefixes: `FUNC`, `SEO`, `SEC`, `UX`, `ACC`, `PERF`, `ARCH`, `P`
- Zero-padded four digits: `SEO0001`
- One defect â†’ one ID forever
- Legacy `NN-###` only in IssueIdMap and historical Changelog notes

## Evidence IDs

- Format `EVnnnn`
- Every cited file needs a Manifest row before report citation
- Missing captures: status **Evidence Not Yet Collected** :  never fabricate

## Report structure

Every report under `Reports/` includes:

1. Purpose  
2. Scope  
3. Methodology  
4. Verified Findings  
5. Evidence References  
6. Risk Analysis  
7. Business Impact  
8. Recommendations  
9. Related Issues  
10. Related Evidence  
11. Related Reports  
12. Conclusion  

## Voice

- Professional, concise, human
- No duplicated boilerplate paragraphs across reports
- Cite Issue IDs instead of restating full register rows
- Do not invent scores

## Linking

- Prefer relative paths from repository root
- Link registers and evidence by path, not by pasted file contents

## Change control

1. New evidence â†’ Manifest row  
2. Status change â†’ IssuesRegister + RemediationValidation + Changelog  
3. Structural change â†’ RepositoryValidation refresh  
4. Readiness/methodology calls â†’ DecisionLog (`DECnnnn`)  
5. Onboarding/IA docs â†’ keep NavigationIndex and ReviewerGuide current  

See also [../RepositoryLifecycle.md](../RepositoryLifecycle.md).
