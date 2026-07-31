# Performance

## Purpose

Document payload and resource signals. Lighthouse/CWV scores are not fabricated (NV0001, EV0019).

## Scope

Homepage, live PDP, all-products collection.

## Methodology

HTML bytes, script counts, lazy/srcset from EV0011.

## Verified Findings

Homepage approximately 590,720 bytes with 67 script tags (**PERF0002**). Primary templates lack srcset (**PERF0001**). Draft merchandising (Coming Soon / ₹0 grids) inflates homepage DOM (**FUNC0002**, **FUNC0003**). Lazy loading is present (CTRL0011). Comparative sizes: home ~591 KB, live PDP ~366 KB, all-products ~287 KB.

## Evidence References

| Evidence ID | See |
|-------------|-----|
| EV0011 | ../Evidence/Reports/TemplateEvidence.jsonl |
| EV0014 | ../Evidence/Home/HomeProbeNotes.md |
| EV0015 | ../Evidence/Products/LivePdpProbeNotes.md |
| EV0019 | Evidence Missing (Lighthouse) |

Metadata: `../Evidence/Metadata/EV0014.md`


## Risk Analysis

Heavy homepage HTML is the paid-landing risk surface.

## Business Impact

Performance debt compounds trust defects when used as an ads destination.

## Recommendations

Remove draft grids first, enable srcset on primary templates, then capture a real Lighthouse export as EV0019.

## Related Issues

PERF0001, PERF0002, FUNC0002, FUNC0003

## Related Evidence

EV0014

## Related Reports

ResponsiveTesting, Seo

## Conclusion

Observable hygiene is weak; lab scores intentionally absent.
