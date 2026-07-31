# Risk Register

Risks derived only from verified issues and decisions already in this release.  
No new findings. No invented financial loss figures.

Risk rating uses qualitative bands: **Critical** · **High** · **Medium** · **Low**  
Numeric loss/probability: **Not Quantified From Verified Evidence**

## Active risks

| Risk ID | Risk | Rating | Linked Issues | Linked Decisions | Mitigation (existing recs) | Residual |
|---------|------|--------|---------------|------------------|----------------------------|----------|
| RSK0001 | Paid traffic lands on unfinished/misleading homepage | Critical | FUNC0001, UX0001, UX0002, FUNC0002, FUNC0003 | DEC0003 | REC0001-REC0005 | Open until P0 Fixed |
| RSK0002 | Consumer/policy exposure from invalid or missing policies | Critical | P0001, P0002, P0003 | DEC0003 | REC0010, REC0011, REC0018 | Open |
| RSK0003 | Weak organic/social foundations on brand root URL | High | SEO0001-SEO0003, SEO0005 | DEC0002 | REC0006-REC0009 | Open |
| RSK0004 | Browse dead ends and empty categories | High | FUNC0004, ARCH0001, ARCH0002 | DEC0001 | REC0012, REC0021, REC0022 | Open |
| RSK0005 | Support journey gap (FAQ unreachable) | High | FUNC0005 | N/A | REC0013 | Open |
| RSK0006 | Accessibility barriers on primary templates | High | SEO0001, ACC0001, ACC0002 | DEC0007 | REC0006, REC0015, REC0028 | Open; tooling EV0018 Missing |
| RSK0007 | Mobile performance risk from heavy homepage / no srcset | High | PERF0001, PERF0002 | DEC0006 | REC0016, REC0017; EV0019 Missing | Open; lab scores NQ |
| RSK0008 | Header hardening incomplete | Medium | SEC0001-SEC0003 | N/A | REC0024-REC0026 | Transport controls remain OK |
| RSK0009 | Stakeholder misunderstanding: docs complete ≠ site ready | Medium | N/A | DEC0004 | STARTHERE / ExecutiveSummary wording | Managed in release docs |
| RSK0010 | Archive credibility if screenshots/lab files are fabricated | Critical (process) | NV0001; EV0017-EV0019 | DEC0006 | Never invent captures | Controlled by process |

## Risk summary

| Band | Count |
|------|------:|
| Critical | 3 (incl. process risk RSK0010) |
| High | 5 |
| Medium | 2 |

## Overall risk (website launch / paid ads)

**Critical** until P0 Issues Fixed with new Evidence IDs (DEC0003).

Financial magnitude: **Not Quantified From Verified Evidence**.

## Related

[IssuesRegister.md](./IssuesRegister.md) · [RecommendationsRegister.md](./RecommendationsRegister.md) · [DecisionLog.md](./DecisionLog.md) · [Reports/BusinessImpact.md](./Reports/BusinessImpact.md)
