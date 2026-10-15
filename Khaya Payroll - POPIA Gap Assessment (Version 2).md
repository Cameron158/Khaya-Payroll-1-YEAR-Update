# Khaya Payroll — POPIA Gap Assessment (Version 2)

## Annual Review — End of Year 1

| Document Control | |
|---|---|
| **Original assessment** | Version 1.0 (Month 0) |
| **This review** | Version 2.0 (Month 12) |
| **Prepared by** | Information Officer & Deputy Information Officer |
| **Next review** | Month 24 |

---

## 1. Purpose & Methodology

This document is the annual review of Khaya Payroll's POPIA compliance posture, measured against the 8 Conditions for Lawful Processing. It updates the original assessment (`03-popia-gap-assessment.md`) to reflect Year 1 remediation progress, the Month 7 security incident, and new risks that emerged during the year.

**Status key used throughout:**

| Status | Meaning |
|---|---|
| ✅ **Closed** | Gap remediated; control in place and functioning |
| 🟡 **In Progress** | Partially remediated; residual gap remains |
| 🔴 **Open** | Gap unresolved; original finding still applies |
| 🆕 **New** | New finding that did not exist in the original assessment |

---

## 2. Updated Scope

| Metric | Original | Year 1 |
|---|---|---|
| Clients | 180 | 256 |
| Staff | 35 | 54 |
| Employee records | ~40,000 | ~67,000 |
| Sub-processors | 4 | 6 (Gusto, Xero added) |

---

## 3. Condition-by-Condition Review

### Condition 1: Accountability (POPIA s8) — ✅ CLOSED

**Original gap:** No Information Officer registered; no Deputy IO; no escalation path.

**Year 1 actions:**

- CEO formally registered as Information Officer with the Information Regulator (Month 1)
- Head of Customer Success appointed as Deputy Information Officer (Month 1)
- Written escalation path documented and distributed to all staff (Month 2)
- IO mandate extended to include security oversight per SOC 2 CC1 recommendation

**Current state:** Fully remediated. The IO/Deputy IO structure functioned as designed during the Month 7 incident — escalation occurred within 1 hour of notification, and the IO activated the incident response plan within 4 hours.

**Residual risk:** Low. The 6-month CC1 role review is now due (see Year 2 priorities) — given 54% staff growth, the combined IO/security role may need to be separated.

**Risk rating:** Low ↓ (was High)

---

### Condition 2: Processing Limitation (POPIA s9–12) — 🟡 IN PROGRESS

**Original gap:** No minimum-necessary standard for medical/leave data; no documented legal basis mapping.

**Year 1 actions:**

- Legal basis mapping document completed and CEO-approved (Month 3) — contract necessity confirmed for payroll data; legal obligation confirmed for SARS/tax data
- Medical/leave data minimum-necessary standard drafted (Month 5) — capturing leave dates and fitness-for-duty status only, no diagnostic detail

**Residual gap:** The medical data standard has been drafted but not yet technically enforced in the platform — HR admins can still upload full medical certificates. Engineering change request submitted (RFC-014); implementation targeted for Month 14.

**Risk rating:** Medium ↓ (was Medium-High)

---

### Condition 3: Purpose Specification (POPIA s13–14) — 🟡 IN PROGRESS

**Original gap:** No privacy notice template; no data retention policy.

**Year 1 actions:**

- Privacy notice template v1.0 published and distributed to all 180 original clients (Month 3)
- Privacy notice updated post-Month 7 incident to include HR admin bulk-email guidance (Month 8)
- Data retention policy written and CEO-approved (Month 4) — 5-year retention period, 2-week access revocation trigger confirmed
- Template distributed to all 256 clients (including 76 new clients) at onboarding

**Residual gap:** Technical enforcement of the retention policy (automated flags for records past the 5-year window) has not been built. Records are managed manually by the Deputy IO on a quarterly basis. Engineering RFC submitted; targeted for Month 15.

**Risk rating:** Medium ↓ (was Medium-High)

---

### Condition 4: Further Processing Limitation (POPIA s15) — 🟡 IN PROGRESS

**Original gap:** No DPAs with sub-processors; no vendor due diligence process.

**Year 1 actions:**

- DPAs signed with Intercom, SendGrid, and Payment Gateway (Month 2)
- SOC 2 Type II reports requested and received for Intercom and Payment Gateway
- ISO 27001 certificate received for SendGrid
- Vendor due diligence checklist created and added to onboarding process
- Two new sub-processors onboarded: Gusto (DPA signed Month 9) and Xero (DPA pending legal review at Month 12)

**Residual gap:** Xero DPA outstanding — Xero onboarded Month 10 for accounting API integration; DPA under external legal review. This is an active POPIA s21 gap. Target resolution: Month 13.

**Risk rating:** Medium ↓ (was Medium-High) — improving but not closed due to Xero DPA gap

---

### Condition 5: Information Quality (POPIA s16) — 🟡 IN PROGRESS

**Original gap:** No validation step for sensitive data field updates; no data quality scans.

**Year 1 actions:**

- Email confirmation step implemented for banking detail updates (Month 5) — employee receives confirmation email before change takes effect
- Quarterly automated data quality scan implemented (Month 6) — flags incomplete fields and duplicate bank account numbers
- First scan (Month 6) identified 14 records with missing tax numbers and 2 duplicate bank account entries — all remediated within 30 days

**Residual gap:** Confirmation step for ID number updates not yet implemented (only banking details currently covered). Targeted for Month 14 as part of RBAC completion work.

**Risk rating:** Medium ↓ (was Medium-High)

---

### Condition 6: Openness (POPIA s17–18) — 🟡 IN PROGRESS

**Original gap:** No ROPA; employees unaware of their POPIA rights.

**Year 1 actions:**

- Employee rights notice (access, correction, objection) published on self-service portal (Month 3)
- HR-led workshop conducted for 12 of 256 client companies (Month 4) — rollout ongoing
- ROPA started (Month 4) — currently 60% complete (payroll and statutory processing sections documented; medical/leave and HR records sections still being scoped)

**Residual gap:** ROPA not yet complete. Medical/leave data section is dependent on the Condition 2 minimum-necessary standard being technically enforced before it can be accurately documented. Target completion: Month 15.

**Risk rating:** Medium ↓ (was High)

---

### Condition 7: Security Safeguards (POPIA s19–22) — 🟡 IN PROGRESS

**Original gap:** Single-factor authentication; no encryption confirmed; broad unlogged internal access; no incident response plan.

**Year 1 actions:**

- MFA enforced for all 54 staff logins (Month 4)
- Access logging implemented — all changes to employee records logged with timestamp, user ID, and field changed (Month 5)
- Weekly access log reviews implemented (IO + IT Head)
- Incident Response Plan v1.0 drafted, CEO-approved (Month 2), and successfully tested in Month 7 incident
- RBAC 3-tier model defined and 60% technically implemented
- Encryption at rest confirmed for ID number fields (Month 8); banking fields in progress

**Residual gaps:**

- RBAC 40% of roles still on legacy broad-access model (engineering in progress)
- Encryption at rest for banking detail fields not yet confirmed
- Device offboarding procedure drafted but inconsistently enforced for remote staff

**Risk rating:** Medium ↓ (was High) — MFA and logging represent significant improvement; RBAC and encryption gaps remain

---

### Condition 8: Data Subject Participation (POPIA s23–25) — 🔴 OPEN

**Original gap:** No data subject request process; no correction confirmations.

**Year 1 actions:**

- Employee rights notice published on self-service portal (Month 3) — employees now informed they have rights
- Update confirmation notification implemented for banking detail changes (Month 5)
- Data subject notification template drafted post-Month 7 incident (Month 8) — available for future breach notifications

**Residual gap:** No formal data subject request form has been built on the portal. Requests submitted informally via support email are handled by the Deputy IO, but without a structured intake form, SLA, or tracking mechanism. This remains the single most significant unresolved POPIA gap at Month 12.

**Risk rating:** High (unchanged) — awareness improved but operational request-handling capability not yet built

---

## 4. New Findings (Year 1)

### Condition 4 (Extended): New Sub-Processor Risk — 🆕 OPEN

Two new sub-processors were onboarded during Year 1 (Gusto, Xero). While Gusto's DPA was completed at onboarding, Xero's DPA remains outstanding. Additionally, the vendor due diligence process — while now documented — has not been formally reviewed since its creation in Month 2, and neither Gusto nor Xero has yet provided a SOC 2 Type II report or ISO 27001 certificate (both have been requested).

### Condition 3 (Extended): Client Bulk-Email Data Handling — 🆕 IN PROGRESS

The Month 7 incident revealed that client HR admins lack sufficient guidance on bulk data handling procedures (e.g. payslip distribution via email). The privacy notice template has been updated and guidance issued, but this has not been tested or verified across all 256 clients. A structured client onboarding checklist addressing this gap was introduced in Month 9 for all new clients; existing clients have not yet completed equivalent training.

---

## 5. Updated Summary Gap Table

| # | Condition | Original Rating | Year 1 Rating | Status |
|---|---|---|---|---|
| 1 | Accountability | High | Low | ✅ Closed |
| 2 | Processing Limitation | Medium-High | Medium | 🟡 In Progress |
| 3 | Purpose Specification | Medium-High | Medium | 🟡 In Progress |
| 4 | Further Processing Limitation | Medium-High | Medium | 🟡 In Progress |
| 5 | Information Quality | Medium-High | Medium | 🟡 In Progress |
| 6 | Openness | High | Medium | 🟡 In Progress |
| 7 | Security Safeguards | High | Medium | 🟡 In Progress |
| 8 | Data Subject Participation | High | High | 🔴 Open |

---

## 6. Year 2 POPIA Priorities

1. **R-011 / Condition 8:** Build data subject request form on self-service portal (highest priority — only remaining High-rated gap)
2. **Condition 4:** Complete Xero DPA; obtain SOC 2/ISO 27001 evidence for Gusto and Xero
3. **Condition 7:** Complete RBAC migration (40% remaining); confirm banking field encryption
4. **Condition 6:** Complete ROPA
5. **Condition 2:** Enforce medical data minimum-necessary standard technically (RFC-014)
6. **All conditions:** Apply COBIT 2019 governance maturity assessment to evaluate control environment quality, not just gap existence

---

*This is Version 2 of a self-directed GRC portfolio assessment using a fictional company. It does not represent a real audit engagement or legal advice.*
