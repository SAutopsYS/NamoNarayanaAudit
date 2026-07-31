# Security

## Purpose

Summarize public security header and transport observations. No penetration testing was performed.

## Scope

Headers on homepage, live PDP, and cart from EV0011; checkout/login redirect observation from EV0001.

## Methodology

Read header fields already captured in TemplateEvidence.jsonl. Summarized in EV0013 without new live calls during repository hardening.

## Verified Findings

HSTS is present (`max-age=7889238`); CTRL0002. CSP is limited to mixed-content blocking, frame-ancestors none, and upgrade-insecure-requests (**SEC0003**). Referrer-Policy and Permissions-Policy are empty (**SEC0001**, **SEC0002**). X-Frame-Options DENY and nosniff were confirmed in the source audit header probes; CTRL0003. Payment completion not tested; NV0005.

## Evidence References

| Evidence ID | See |
|-------------|-----|
| EV0013 | ../Evidence/Headers/SecurityHeadersSummary.md |
| EV0011 | ../Evidence/Reports/TemplateEvidence.jsonl |
| EV0021 | ../Evidence/Checkout/CheckoutEntryNotes.md |
| EV0026 | Evidence Cannot Be Collected (payment proof) |

Metadata: `../Evidence/Metadata/EV0013.md`


## Risk Analysis

Transport is acceptable. Header hardening is incomplete. Content-trust defects elsewhere remain the larger business risk.

## Business Impact

Missing referrer/permissions policies are hardening debt, not evidence of active compromise.

## Recommendations

Add Referrer-Policy and Permissions-Policy where Shopify/Cloudflare configuration allows; revisit CSP feasibility.

## Related Issues

SEC0001, SEC0002, SEC0003

## Related Evidence

EV0013

## Related Reports

ProductionGovernance gates referencing CTRL0002/CTRL0003

## Conclusion

Partial security readiness: transport yes, policy headers incomplete.
