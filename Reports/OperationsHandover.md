# Operations Handover

## Purpose

Ordered remediation runbook for store operators and developers.

## Scope

Open Issue IDs with public acceptance tests. No staffing SLAs claimed.

## Methodology

Sequence by buyer-trust impact; acceptance tests are HTTP/HTML checks that mint new EV IDs when re-run.

## Verified Findings (action sequence)

| Step | Issue ID | Action | Acceptance |
|------|----------|--------|------------|
| 1 | FUNC0001 | Remove sample products | Homepage Sample Product count = 0 |
| 2 | FUNC0002, FUNC0003 | Draft ₹0/unavailable SKUs; clear Coming Soon grids | Homepage coming/rs0 near zero |
| 3 | UX0001, UX0002 | Remove `0+` and `10,000+` claims | No matches on `/` |
| 4 | P0001 | Rewrite refund for food; real address | No INSERT; no unworn |
| 5 | P0002 | Fix shipping policy | Stable HTTP 200 |
| 6 | FUNC0005 | Publish FAQ or remove links | 200 page or zero FAQ hrefs |
| 7 | SEO0001, SEO0002, SEO0005 | Homepage H1, meta, og:image | Present in source |
| 8 | SEO0003 | JSON-LD Organization + Product | ld+json ≥ 1 on home and PDP |
| 9 | FUNC0004 | Fix collection handles | Bad URLs gone or 301 |
| 10 | P0003 | Single NAP everywhere | Footer = privacy = contact |

Then address P1 queue in IssuesRegister.

## Evidence References

| Evidence ID | See |
|-------------|-----|
| EV0014 | ../Evidence/Home/HomeProbeNotes.md (baseline) |
| EV0016 | ../Evidence/Policies/RefundPolicyProbeNotes.md (baseline) |
| EV0001 | ../Evidence/Discovery/DiscoveredPages.csv (baseline) |

After remediation, mint **new** Evidence IDs; do not overwrite baselines.


## Risk Analysis

Partial fixes (meta only) leave trust defects intact.

## Business Impact

This sequence is the shortest path to a defendable relaunch.

## Recommendations

Execute steps 1-10, re-probe, update RemediationValidation and IssuesRegister statuses.

## Related Issues

All P0 IDs

## Related Evidence

EV0014, EV0016

## Related Reports

RemediationValidation, ProductionGovernance

## Conclusion

Ops path is clear; execution is outstanding.
