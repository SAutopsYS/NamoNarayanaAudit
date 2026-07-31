# Responsive Testing

## Purpose

Document responsive-delivery signals available without device lab screenshots.

## Scope

Homepage, live PDP, collection, cart, search (comparative srcset behavior).

## Methodology

Compare srcset, lazy-loading, and HTML bytes from EV0011. Device screenshots: Evidence Not Yet Collected (EV0017, NV0002).

## Verified Findings

Homepage, PDP, and collection probes show srcset count 0 (**PERF0001**). Search hit probe shows srcset count 6, proving the pipeline can emit responsive sources. Homepage HTML is approximately 591 KB with 67 scripts (**PERF0002**). Lazy loading is present on the homepage (CTRL0011).

## Evidence References

| Evidence ID | See |
|-------------|-----|
| EV0011 | ../Evidence/Reports/TemplateEvidence.jsonl |
| EV0014 | ../Evidence/Home/HomeProbeNotes.md |
| EV0024 | ../Evidence/Search/SearchProbeNotes.md |
| EV0017 | Evidence Missing (device screenshots) |

Metadata: `../Evidence/Metadata/EV0024.md`


## Risk Analysis

Paid traffic landing on homepage inherits the weakest responsive image behavior.

## Business Impact

Mobile load risk without claiming unverified CWV scores (NV0001).

## Recommendations

Align home/PDP/collection image output with search srcset behavior; trim homepage sections.

## Related Issues

PERF0001, PERF0002

## Related Evidence

EV0011, EV0014

## Related Reports

Performance

## Conclusion

Responsive hooks exist unevenly; primary templates remain weak on srcset.
