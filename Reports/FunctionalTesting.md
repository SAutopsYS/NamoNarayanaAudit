# Functional Testing

## Purpose

Validate public commerce and support journeys against discovered URLs only.

## Scope

Search, cart, checkout entry, live PDP, contact page presence, refund content, shipping/FAQ availability, broken collection handles. Payment completion excluded (NV0005).

## Methodology

HTTP/HTML probes and title checks recorded in EV0001 and EV0011. Redirects followed for checkout and login.

## Verified Findings

| Issue ID | Observation | Status |
|----------|-------------|--------|
| CTRL0004 | Search hit (5 results for ghee) and zero-result path work | ✅ |
| CTRL0005 | Cart returns 200 | ✅ |
| CTRL0006 | Checkout redirects to `/checkouts/cn/...` | ✅ |
| FUNC0001 | Sample products on homepage (count 4) | ❌ |
| FUNC0003 | Zero-price unavailable SKUs still published | ❌ |
| FUNC0004 | Four collection handles unreachable | ❌ |
| FUNC0005 | FAQ unreachable; absent from pages.json | ❌ |
| FUNC0006 | Turmeric chip present without turmeric SKU | ❌ |
| P0001 | Refund contains INSERT RETURN ADDRESS and unworn | ❌ |
| P0002 | Shipping policy unreachable though footer-linked | ❌ |
| NV0004 | Form inbox delivery not exercised | ⚪ |

## Evidence References

| Evidence ID | See |
|-------------|-----|
| EV0001 | ../Evidence/Discovery/DiscoveredPages.csv |
| EV0011 / EV0012 | ../Evidence/Reports/TemplateEvidence.jsonl |
| EV0016 | ../Evidence/Policies/RefundPolicyProbeNotes.md |
| EV0021 | ../Evidence/Checkout/CheckoutEntryNotes.md |
| EV0023 | ../Evidence/Navigation/BrokenCollectionHandles.md |
| EV0024 | ../Evidence/Search/SearchProbeNotes.md |
| EV0025 | Evidence Cannot Be Collected (form delivery) |
| EV0026 | Evidence Cannot Be Collected (payment completion) |

Metadata: `../Evidence/Metadata/EV0016.md`, `EV0021.md`, `EV0024.md`


## Risk Analysis

Purchase start works; policy and support paths do not.

## Business Impact

Chargeback and pre-purchase trust risk from P0001/P0002 outweigh residual search polish.

## Recommendations

Stabilize shipping and FAQ, rewrite refund, remove sample and ₹0 surfaces, fix collection handles.

## Related Issues

FUNC0001, FUNC0003, FUNC0004, FUNC0005, FUNC0006, P0001, P0002

## Related Evidence

EV0001, EV0011, EV0012, EV0016, EV0021, EV0023, EV0024 (EV0025-EV0026 Cannot Be Collected)

## Related Reports

Documentation, OperationsHandover, RemediationValidation

## Conclusion

Commerce entry is operable. Support and policy functions are not launch-ready.
