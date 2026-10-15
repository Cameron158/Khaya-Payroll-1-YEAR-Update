# Khaya Payroll — SOC 2 Gap Analysis (Version 2)
## Annual Review — End of Year 1

**Original assessment:** Version 1.0 (Month 0)
**This review:** Version 2.0 (Month 12)
**Prepared by:** Information Officer & Deputy Information Officer
**Next review:** Month 24

---

## 1. Purpose & Methodology

This document reviews Khaya Payroll's SOC 2 posture against the Trust Services Criteria (Security CC1–CC9, Availability A1) at the end of Year 1. It updates the original SOC 2 Gap Analysis (`04-soc2-gap-analysis.md`) to reflect remediation progress, the Month 7 incident, and new risks.

**Status key:**
- ✅ **Closed** — gap remediated; control in place
- 🟡 **In Progress** — partially remediated; residual gap remains
- 🔴 **Open** — gap unresolved
- 🆕 **New** — new finding not in original assessment

---

## 2. Updated Scope

| Metric | Original | Year 1 |
|---|---|---|
| Clients | 180 | 256 |
| Staff | 35 | 54 |
| Employee records | ~40,000 | ~67,000 |
| Sub-processors | 4 | 6 |

---

## 3. Category-by-Category Review

### CC1: Control Environment — ✅ CLOSED

**Original gap:** No security ownership; no security policy; no governance structure.

**Year 1 actions:**
- IO mandate formally extended to include security oversight (Month 1)
- Security policy v1.0 drafted and CEO-approved (Month 3)
- Monthly security check-ins established (IO + IT Head) — 8 of 10 completed
- Quarterly deep-dive reviews established — 2 of 3 completed

**Residual consideration:** The 6-month role review is now overdue. Given 54% staff growth and the Month 7 incident workload, the combined IO/security role is showing signs of strain. Year 2 priority: formally evaluate whether a dedicated Security Lead is warranted.

**Risk rating:** Low ↓ (was High)

---

### CC2: Communication & Information — ✅ CLOSED

**Original gap:** No internal reporting channel; no external disclosure policy.

**Year 1 actions:**
- security@khayapayroll.co.za established (Month 2)
- Responsible disclosure policy published on company website (Month 2)
- Anonymous internal reporting channel implemented via HR platform (Month 4)
- Security awareness training — 1 of 4 quarterly sessions delivered (Month 4)

**Residual gap:** Only 1 of 4 security awareness training sessions delivered. With 54% staff growth, a significant proportion of new staff have not yet received training. This is escalated as a new risk (R-022) rather than a CC2 gap, since the channel and policy are in place — the gap is now execution/frequency rather than existence of the control.

**Risk rating:** Low ↓ (was Medium-High)

---

### CC3: Risk Assessment — 🟡 IN PROGRESS

**Original gap:** No formal risk assessment process; reactive rather than proactive.

**Year 1 actions:**
- Monthly risk check-ins established (Month 2) — 8 of 10 completed on schedule
- Quarterly deep-dive risk register reviews established — 2 of 3 completed (Q3 missed due to enterprise client onboarding)
- Pre-implementation risk review process introduced for new integrations — applied to Gusto and Xero onboarding

**Residual gap:** Cadence inconsistency — 2 monthly check-ins and 1 quarterly deep-dive were missed. The Q3 review gap means some risks were not formally reviewed for approximately 5 months. Consistency improvement is a Year 2 priority.

**Risk rating:** Medium ↓ (was Medium-High)

---

### CC4: Monitoring Activities — 🟡 IN PROGRESS

**Original gap:** No mechanism to verify controls are functioning as intended.

**Year 1 actions:**
- Monthly control sign-off checklist implemented (Month 3) — IO and IT Head sign off monthly
- Quarterly control effectiveness review folded into CC3 deep-dive cadence
- Weekly access log reviews running consistently since Month 5
- Nessus Essentials weekly scans running since Month 3 — 3 medium findings identified and remediated

**Residual gap:** Sign-off checklist completion rate mirrors the CC3 cadence gap — 8 of 10 monthly check-ins completed. The 2 missed months represent a monitoring gap where control effectiveness was unverified.

**Risk rating:** Medium ↓ (was Medium-High)

---

### CC5: Control Activities — ✅ CLOSED

**Original gap:** No formally adopted policies or procedures; recommendations not operationalized.

**Year 1 actions:**
- Standard policy template (purpose, scope, procedure, owner, review date) established and CEO-approved (Month 3)
- Access Control Policy v1.0 drafted, CEO-approved, and distributed (Month 3)
- Incident Response Policy v1.0 drafted, CEO-approved, and distributed (Month 2)
- Both policies successfully applied during Month 7 incident
- Vendor Management Policy: not yet drafted (deferred to Month 13)

**Residual gap:** Vendor Management Policy outstanding. However, the vendor register (CC9) and existing DPA process cover the operational need in the interim. CC5 is considered closed for the policies that exist; Vendor Management Policy is tracked as an open item.

**Risk rating:** Low ↓ (was High)

---

### CC6: Logical & Physical Access Controls — 🟡 IN PROGRESS

**Original gap:** Single-factor auth; no MFA; no device policy; no building access controls.

**Year 1 actions:**
- MFA enforced for all 54 staff logins (Month 4) — 100% compliance
- RBAC 3-tier model defined (Month 2); 60% technically implemented (Month 12)
- Access logging live since Month 5
- Device offboarding procedure drafted (Month 4)
- Full-disk encryption required for all new staff laptops (policy effective Month 5)
- ID badge access control system installed at Cape Town office (Month 6)

**Residual gaps:**
- RBAC 40% still on legacy broad-access model (12 engineering staff, 3 finance staff)
- Encryption at rest for banking fields not yet confirmed
- Device offboarding enforcement inconsistent for remote staff (7 of 19 remote departures in Year 1 had delayed device return beyond 2-week policy)

**Risk rating:** Medium ↓ (was Medium-High)

---

### CC7: System Operations — 🟡 IN PROGRESS

**Original gap:** No monitoring; no vulnerability scanning; no tested IRP.

**Year 1 actions:**
- Native login anomaly alerting enabled (Month 2) — flags failed logins (5+ attempts) and new-location logins
- Weekly Nessus Essentials vulnerability scans running since Month 3
- 3 medium vulnerabilities identified and remediated (Month 5, Month 8, Month 11)
- 0 critical vulnerabilities identified
- IRP tested in live Month 7 incident — functioned as designed
- Tabletop exercise completed Month 9 (ransomware + accidental-disclosure scenarios)

**Residual gap:** No dedicated SIEM or enterprise monitoring tool — native alerting only. As client and staff count grows, the volume and complexity of security events may exceed the capacity of native alerting to surface. Year 2 consideration: evaluate whether a lightweight SIEM (e.g. Wazuh, free and open-source) is warranted.

**Risk rating:** Medium ↓ (was High)

---

### CC8: Change Management — ✅ CLOSED

**Original gap:** No change management process; no records; no rollback plan.

**Year 1 actions:**
- GitLab implemented as authoritative change log (Month 2) — all code changes version-controlled
- RFC template v1.0 approved and enforced for all changes since Month 3
- Pre-change approval process: all RFCs reviewed by IT Head before deployment
- Revert process defined and documented in RFC template
- 0 production incidents attributable to unreviewed changes in Year 1
- Emergency change process defined (expedited RFC + mandatory post-implementation review)

**Risk rating:** Low ↓ (was High)

---

### CC9: Risk Mitigation — 🟡 IN PROGRESS

**Original gap:** No vendor register; no business continuity plan; no client communication plan.

**Year 1 actions:**
- Vendor register built and maintained by IO (Month 2) — 6 vendors documented
- DPAs signed for 5 of 6 vendors (Xero pending)
- Infrastructure redundancy/failover system live (Month 6)
- Manual payroll fallback process documented (Month 8) — not yet tested
- Client communication plan finalized (Month 5) — 8-hour notification window
- Month 7 incident tested the client communication plan successfully

**Residual gaps:**
- Xero DPA outstanding
- Manual payroll fallback not tested with a real client dry-run
- 2 of 4 original vendors (Intercom, Gusto) have not yet provided renewed SOC 2/ISO 27001 evidence (requests sent Month 10)

**Risk rating:** Medium ↓ (was High)

---

### A1: Availability — ✅ CLOSED

**Original gap:** No SLA; no uptime monitoring; no capacity planning.

**Year 1 actions:**
- SLA (99% uptime commitment) included in all new client contracts since Month 3
- UptimeRobot monitoring live since Month 3 — 99.2% uptime achieved vs 99% target
- 2 minor outages in Year 1 (Month 5: 47 minutes; Month 9: 23 minutes) — both within SLA allowance
- Annual capacity planning review completed Month 11 — infrastructure upgrade recommended for Q1 Year 2 to support continued growth
- Capacity trigger review: client count grew 42% — triggers the >20% growth threshold; infrastructure upgrade formally approved

**Risk rating:** Low ↓ (was Medium-High)

---

## 4. New Findings (Year 1)

### CC2 / CC7: Security Training Coverage Gap — 🆕 OPEN

Only 1 of 4 quarterly security awareness training sessions was delivered in Year 1. With 54% staff growth, approximately 22 new staff members have not received any formal security training. This increases phishing susceptibility and reduces the effectiveness of the anonymous reporting channel (staff can't report what they don't recognize). **Risk rating: Medium-High**

### CC9: New Sub-Processor Gaps (Gusto, Xero) — 🆕 IN PROGRESS

Gusto DPA signed; Xero DPA outstanding. Neither has provided SOC 2/ISO 27001 evidence. **Risk rating: Medium**

### CC3: Review Cadence Inconsistency — 🆕 IN PROGRESS

2 monthly check-ins and 1 quarterly review were missed in Year 1. Controls were unverified for approximately 2 months cumulatively. **Risk rating: Low-Medium**

---

## 5. Updated Summary Gap Table

| # | Category | Original Rating | Year 1 Rating | Status |
|---|---|---|---|---|
| 1 | CC1: Control Environment | High | Low | ✅ Closed |
| 2 | CC2: Communication & Information | Medium-High | Low | ✅ Closed |
| 3 | CC3: Risk Assessment | Medium-High | Medium | 🟡 In Progress |
| 4 | CC4: Monitoring Activities | Medium-High | Medium | 🟡 In Progress |
| 5 | CC5: Control Activities | High | Low | ✅ Closed |
| 6 | CC6: Logical & Physical Access Controls | Medium-High | Medium | 🟡 In Progress |
| 7 | CC7: System Operations | High | Medium | 🟡 In Progress |
| 8 | CC8: Change Management | High | Low | ✅ Closed |
| 9 | CC9: Risk Mitigation | High | Medium | 🟡 In Progress |
| 10 | A1: Availability | Medium-High | Low | ✅ Closed |

**Closed: 5 of 10 | In Progress: 4 of 10 | Open: 0 of 10 (1 new finding open)**

---

## 6. Year 2 SOC 2 Priorities

1. Complete RBAC technical implementation (CC6)
2. Confirm banking field encryption at rest (CC6/CC7)
3. Deliver remaining 3 security awareness training sessions — prioritise new staff (CC2/CC7)
4. Complete Xero DPA and obtain vendor evidence for Gusto and Xero (CC9)
5. Test manual payroll fallback with client dry-run (CC9)
6. Evaluate SIEM tooling for Year 2 (CC7)
7. Conduct formal CC1 role review — dedicated Security Lead evaluation
8. Apply COBIT 2019 framework — governance maturity assessment
9. Apply ITIL 4 framework — service management maturity assessment

---

*This is Version 2 of a self-directed GRC portfolio assessment using a fictional company. It does not represent a real audit engagement or legal advice.*
