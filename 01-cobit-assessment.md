# Khaya Payroll — COBIT 2019 Governance Maturity Assessment
## Year 2 Assessment | Baseline: Month 12 (End of Year 1)

**Framework:** COBIT 2019 (ISACA)
**Assessment date:** Month 13 (Start of Year 2)
**Prepared by:** Information Officer & Deputy Information Officer
**Next review:** Month 24 (End of Year 2)
**Document version:** 1.0 (in progress)

---

## 1. Purpose & Methodology

This document assesses Khaya Payroll's IT governance and management maturity against the COBIT 2019 framework. Where the POPIA and SOC 2 assessments asked "are specific controls in place?", this COBIT assessment asks a broader question:

> **"Is IT being governed and managed in a way that creates value for the business while managing risk and using resources efficiently?"**

COBIT 2019 covers 40 governance and management objectives across 5 domains. This assessment focuses on the 12 objectives most relevant to Khaya Payroll's size, risk profile, and the gaps identified in the Year 1 POPIA and SOC 2 reviews.

Each objective is assessed using a five-part structure:
1. **Objective summary** — what COBIT requires, in plain English
2. **Current state** — what Khaya Payroll does today (Month 12 baseline)
3. **Current maturity** — rating on the 0–5 COBIT capability scale, with reasoning
4. **Target maturity** — realistic target for end of Year 2, with justification
5. **Gap & Recommendation** — what needs to change to reach target maturity

---

## 2. COBIT 2019 Maturity Scale

| Level | Label | What it means for Khaya Payroll |
|---|---|---|
| 0 | Incomplete | Process not performed or consistently fails to achieve its purpose |
| 1 | Performed | Process achieves its purpose but informally — relies on individuals, not structure |
| 2 | Managed | Process is planned, monitored, and adjusted — some documentation and ownership exists |
| 3 | Established | Process uses a defined, standardized, documented approach consistently followed |
| 4 | Predictable | Process operates within defined limits; outcomes are consistent and measurable |
| 5 | Optimizing | Process continuously improves to meet changing business and risk goals |

**Note:** For a 54-person SaaS startup at Month 12, Level 2–3 is the realistic and appropriate target range for most objectives. Level 4–5 is typically large enterprise territory and is not targeted in this assessment cycle.

---

## 3. Domains and Objectives Assessed

| Domain | Objectives assessed |
|---|---|
| **EDM** — Evaluate, Direct, Monitor | EDM01, EDM03, EDM05 |
| **APO** — Align, Plan, Organise | APO01, APO12, APO13 |
| **BAI** — Build, Acquire, Implement | BAI06, BAI10 |
| **DSS** — Deliver, Service, Support | DSS02, DSS04, DSS05 |
| **MEA** — Monitor, Evaluate, Assess | MEA01, MEA03 |

---

## 4. Overall Maturity Assessment — Month 12 Baseline

At Month 12, Khaya Payroll operates at an overall COBIT maturity level of **2 (Managed)**. This reflects significant progress from Month 0, where all processes were performed informally and ad hoc — the CEO handled all governance, compliance, and security decisions without documentation, assigned ownership, or defined process. By Month 12, core foundations are in place: an Information Officer registered, policies drafted and CEO-approved, security controls (MFA, logging, change management, incident response) implemented and tested in a live incident, and governance meetings established.

However, Level 3 (Established) has not yet been achieved because key processes lack consistency and standardization — security awareness training has not been delivered at the planned quarterly cadence, role-based access control remains incomplete, device offboarding enforcement is patchy for remote staff, and several critical documents (ROPA, data subject request form) remain unfinished.

The Year 2 COBIT assessment targets Level 3 for most governance objectives, with the most mature processes (change management, incident response, availability monitoring) potentially reaching Level 3 already, and the weakest processes (training, access control, data subject participation) requiring focused remediation before Level 3 is achievable.

---

## 5. Domain-by-Domain Assessment

### EDM Domain — Evaluate, Direct, Monitor

---

### EDM01: Governance Framework Setting and Maintenance

**Objective summary:** Leadership must establish and maintain a governance framework defining how IT decisions are made, who holds authority, how performance is monitored, and how IT governance aligns to overall business objectives.

**Current state (Month 12):** Khaya Payroll has established foundational governance elements — a registered Information Officer, CEO-approved policies, and monthly and quarterly review cadences — but has not yet defined a formal IT governance framework governing how all IT decisions are made, escalated, and aligned to business objectives. Major IT decisions (infrastructure investments, vendor selection, system changes) are currently made informally by a small group of individuals (CEO, IO, IT Head) without a structured decision-making process, defined authority matrix, or board-level IT oversight. The monthly and quarterly review cadence established in Year 1 provides operational monitoring of security controls, but does not constitute a governance framework — it lacks the strategic direction-setting, resource allocation oversight, and performance-against-objectives evaluation that a formal IT governance structure would require.

**Current maturity:** Level 2 (Managed) — Khaya Payroll has progressed beyond informal, ad hoc IT governance (Level 1) through the establishment of an Information Officer role, CEO-approved policies, and structured review cadences. However, Level 3 has not been achieved because no formal, documented IT governance framework exists that defines decision-making authority, escalation paths, or how IT strategy aligns to business objectives — governance remains dependent on a small group of individuals rather than a standardized, repeatable process.

**Target maturity:** Level 2 (Managed) — Level 2 remains the appropriate target for Year 2 given Khaya Payroll's size and competing remediation priorities. However, as the company scales toward 300+ clients and 70+ staff, the current informal governance model will become inadequate and Level 3 will need to be targeted in Year 3.

**Gap:** No formal IT governance framework or decision rights document exists. The CC1 role review (scheduled at Month 6) is overdue at Month 12.

**Recommendation:** Conduct the overdue CC1 role review to formally assess whether Khaya Payroll's 54% staff growth and increasing compliance obligations now warrant a dedicated Security Lead, rather than continuing to extend the IO's mandate indefinitely. Additionally, produce a lightweight decision rights document (one page) capturing who holds authority for each category of IT decision (infrastructure, vendor selection, system changes, policy approval) and when escalation to CEO level is required — providing a practical governance reference proportionate to Khaya Payroll's current size, without the overhead of a full IT governance framework.

---

## EDM03: Risk Optimisation

**Objective summary:** Leadership must ensure the organization's risk appetite and tolerance are defined and understood, that IT-related risk is identified and managed within those boundaries, and that risk information is reported to leadership on an ongoing, scheduled basis — not only when incidents occur.

**Current state (Month 12):** Khaya Payroll has not defined a formal risk appetite or risk tolerance statement — there is no documented position on how much risk leadership is willing to accept before escalation or action is required. While a risk register exists (v1 and v2, 24 risks with 8 closed) and monthly and quarterly reviews have been established per CC3, IT-related risk is reported to leadership reactively rather than on a defined, scheduled basis. The Month 7 incident illustrates this gap: leadership was not proactively aware of the client-side bulk-email handling risk before it materialised — it only became visible when the incident occurred, rather than through a structured risk reporting mechanism that might have surfaced it earlier. The existing review cadence provides operational monitoring of controls, but does not constitute risk optimisation — it lacks a defined appetite against which risk decisions can be measured, and does not deliver a structured risk report to leadership.

**Current maturity:** Level 2 (Managed) — a risk register exists and monthly and quarterly review cadences have been established, representing clear progress beyond purely reactive risk management (Level 1). However, Level 3 has not been achieved because no formal risk appetite or tolerance statement has been defined, and IT-related risk is not reported to leadership on a structured, scheduled basis — leadership visibility remains event-driven rather than systematic.

**Target maturity:** Level 3 (Established) — unlike EDM01, Level 3 is an appropriate and achievable target for Year 2, because the risk register and review cadence already exist. The missing pieces are documentary and procedural rather than structural: a formal risk appetite statement and a defined quarterly reporting schedule. Both are relatively low-lift given the foundations already in place.

**Gap:** No formal risk appetite or tolerance statement exists, and no scheduled IT risk reporting mechanism to leadership is in place. Risk information reaches leadership only when an incident occurs.

**Recommendation:** The Information Officer drafts a one-page risk appetite statement for CEO approval — zero tolerance for risks to the confidentiality or integrity of employee PII and payroll data (ID numbers, banking details), low tolerance for platform availability risks given contractual monthly payroll deadlines, and moderate tolerance for operational and process risks with no direct client data or payroll impact. Additionally, the IO should present a quarterly risk report to the executive leadership team in slide-deck format, structured around the three appetite tiers, with zero-tolerance exceptions tabled first and risk register movement (new, closed, re-rated risks) reported against the prior quarter.

---

*Remaining objectives (EDM05, APO01, APO12, APO13, BAI06, BAI10,
DSS02, DSS04, DSS05, MEA01, MEA03) in progress.*

---

*This assessment is a self-directed GRC portfolio exercise using a
fictional company. It does not represent a real audit engagement or
legal advice.*
