# Evidence Gap Register

Tracks evidence that is **Missing** or **Cannot Be Collected**.  
Does not create new audit findings. Complements [EvidenceManifest.md](./EvidenceManifest.md).

Priority: P0 = blocks visual/client confidence for open P0 issues · P1 = strengthens verification · P2 = archival nice-to-have


### EV0017: Screenshots (home, PDP, policies, journeys)
| Field | Value |
|-------|-------|
| Reason Missing | Visual capture not performed in source public audit |
| Business Impact | Harder for non-technical stakeholders to “see” trust defects |
| Verification Impact | Metrics still verified via EV0011/EV0014/EV0016; visual corroboration absent |
| Can It Be Collected Later | Yes |
| Recommended Collection Method | Annotated browser screenshots; store under Evidence/Screenshots; new SHA256 metadata |
| Priority | P0 |
| Current Status | Evidence Missing |

### EV0018: axe / WAVE export
| Field | Value |
|-------|-------|
| Reason Missing | Automated a11y tooling not run/retained |
| Business Impact | Limited formal WCAG tooling proof |
| Verification Impact | Observable HTML defects (H1/alt) remain evidenced in EV0014/EV0015 |
| Can It Be Collected Later | Yes |
| Recommended Collection Method | axe DevTools or WAVE export JSON/HTML → Evidence/Accessibility |
| Priority | P1 |
| Current Status | Evidence Missing |

### EV0019: Lighthouse report
| Field | Value |
|-------|-------|
| Reason Missing | Lab run not retained (NV0001); scores never invented |
| Business Impact | No numeric CWV/lab score for stakeholders |
| Verification Impact | Payload/script/srcset hygiene still evidenced (EV0014, EV0011) |
| Can It Be Collected Later | Yes |
| Recommended Collection Method | PageSpeed Insights or Lighthouse JSON/HTML/PDF → Evidence/Performance |
| Priority | P1 |
| Current Status | Evidence Missing |

### EV0020: Full page HTML archives
| Field | Value |
|-------|-------|
| Reason Missing | Full HTML not stored; metrics extracted into EV0011 |
| Business Impact | Low if EV0011 retained; harder forensic re-parse of exact markup later |
| Verification Impact | Minimal for current conclusions |
| Can It Be Collected Later | Yes |
| Recommended Collection Method | Save sanitized HTML per template → Evidence/HTML; hash + Manifest |
| Priority | P2 |
| Current Status | Evidence Missing |

### EV0025: Contact form delivery proof
| Field | Value |
|-------|-------|
| Reason Missing | Submit/inbox verification out of public-probe scope (NV0004) |
| Business Impact | Unknown ops reliability of contact form |
| Verification Impact | Form presence tested; delivery not |
| Can It Be Collected Later | Yes (with inbox access) |
| Recommended Collection Method | Controlled submit + mailbox screenshot/EML; redact PII |
| Priority | P1 |
| Current Status | Evidence Cannot Be Collected (this engagement) |

### EV0026: Payment completion proof
| Field | Value |
|-------|-------|
| Reason Missing | Payment requires buyer approval; agent checkout completion excluded (NV0005) |
| Business Impact | Unknown payment success rate |
| Verification Impact | Checkout **entry** still verified (EV0021, CTRL0006) |
| Can It Be Collected Later | Yes (staged human order) |
| Recommended Collection Method | Test order with real/buyer-approved payment; redact secrets |
| Priority | P1 |
| Current Status | Evidence Cannot Be Collected (this engagement) |

### EV0027: HTTP status bodies for aborted URLs
| Field | Value |
|-------|-------|
| Reason Missing | Connection closed before status body (NV0006) |
| Business Impact | Shipping/FAQ/bad handles recorded as UNREACHABLE rather than typed 404 |
| Verification Impact | Reachability failure still proven in EV0001 for affected URLs |
| Can It Be Collected Later | Partially (retry from other networks/tools) |
| Recommended Collection Method | curl/HAR from multiple egress points; store headers/body if obtained |
| Priority | P1 |
| Current Status | Evidence Cannot Be Collected (this engagement) |


## Summary

| Status | Count |
|--------|------:|
| Evidence Missing | 4 |
| Evidence Cannot Be Collected | 3 |
| Highest priority gap | EV0017 screenshots |

Closing gaps must not alter Issue severity without new verified observations logged as new Evidence IDs.

