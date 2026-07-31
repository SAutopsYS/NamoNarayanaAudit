# Accessibility

## Purpose

Record observable accessibility defects from public HTML. Tooling dumps and keyboard screenshots are not in the archive.

## Scope

Homepage, collection, PDP, contact, search, cart, refund policy.

## Methodology

Count H1 and empty alt attributes from EV0011. axe/WAVE: Evidence Not Yet Collected (EV0018). Contrast and focus: NV0002, NV0003.

## Verified Findings

Homepage has zero H1 elements (**SEO0001**: primary ID; accessibility impact acknowledged here without a second ID). Cart has two H1 elements (**ACC0002**). Empty or missing alt appears on homepage (13/71) and live PDP (15/46) (**ACC0001**). Other sampled templates generally expose one H1 (CTRL0009).

## Evidence References

| Evidence ID | See |
|-------------|-----|
| EV0011 / EV0012 | ../Evidence/Reports/TemplateEvidence.jsonl |
| EV0014 | ../Evidence/Home/HomeProbeNotes.md |
| EV0015 | ../Evidence/Products/LivePdpProbeNotes.md |
| EV0018 | Evidence Missing (axe/WAVE) |

Metadata: `../Evidence/Metadata/EV0014.md`, `EV0015.md`


## Risk Analysis

Landing-page heading failure is high impact because `/` is the default campaign URL.

## Business Impact

Assistive technology users and SEO share the same structural defect on home.

## Recommendations

Add homepage H1, fix content image alts, reduce cart to one H1, then run automated and keyboard passes (collect EV0018).

## Related Issues

SEO0001, ACC0001, ACC0002

## Related Evidence

EV0014, EV0015

## Related Reports

Seo, UiReview

## Conclusion

Observable a11y bar is not met; deeper conformance remains unverified.
