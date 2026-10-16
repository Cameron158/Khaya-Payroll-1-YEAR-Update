# Khaya Payroll — POPIA & SOC 2 Readiness Assessment
## Year 1 Review | GRC Portfolio Project

A hands-on GRC portfolio project simulating a real-world compliance readiness assessment and annual review cycle for a fictional South African HR/Payroll SaaS company, **Khaya Payroll (Pty) Ltd**.

This project demonstrates a complete GRC analyst workflow across two years of engagement:
- **Year 0 (Month 0):** Initial POPIA and SOC 2 gap assessments, data flow diagram, risk register
- **Year 1 (Month 12):** Annual review, incident response, remediation tracking, updated risk register
- **Year 2 (in progress):** COBIT 2019 governance maturity assessment + ITIL 4 service management assessment

---

## Project Scenario

Khaya Payroll is a Cape Town-based SaaS platform providing cloud payroll and HR management to South African SMEs. After signing its first large enterprise client — whose procurement team required proof of POPIA compliance and a SOC 2 report — Khaya Payroll commissioned a readiness assessment ahead of engaging an external auditor.

**Year 1 highlights:**
- Grew from 180 → 256 clients, 35 → 54 staff, ~40,000 → ~67,000 employee records
- Experienced one reportable security incident (Month 7: accidental payslip disclosure)
- Incident response plan activated and validated; Information Regulator notified within 72-hour benchmark
- No regulatory enforcement action taken
- Phase 1 remediation complete; Phase 2 ~70% complete; Phase 3 started

---

## Repository Structure

| File | Description | Status |
|---|---|---|
| `README.md` | This file — project overview and repo structure | ✅ Current |
| `01-company-scope.md` | Company profile, data inventory, architecture, assessment scope | ✅ Complete |
| `02-data-flow-diagram/` | draw.io data flow diagram (source `.drawio` + exported `.svg`) | ✅ Complete |
| `03-popia-gap-assessment.md` | Original POPIA gap assessment — 8 conditions, risk ratings, roadmap | ✅ Baseline |
| `03-popia-gap-assessment-v2.md` | Year 1 POPIA review — updated findings, incident impact, new risks | ✅ Complete |
| `04-soc2-gap-analysis.md` | Original SOC 2 gap analysis — CC1–CC9 + A1, roadmap | ✅ Baseline |
| `04-soc2-gap-analysis-v2.md` | Year 1 SOC 2 review — updated findings, 5 categories closed | ✅ Complete |
| `05-risk-register/khaya-payroll-risk-register-v1.xlsx` | Original risk register — 21 risks (Month 0) | ✅ Baseline |
| `05-risk-register/khaya-payroll-risk-register-v2.xlsx` | Updated risk register — 24 risks, Year 1 status, 8 risks closed | ✅ Complete |
| `06-policies/` | Sample policies (Access Control, Incident Response, Vendor Management) | 🟡 In Progress |
| `07-executive-summary.md` | Executive summary for non-technical stakeholders | 🔴 Planned |
| `08-cobit-assessment.md` | COBIT 2019 governance maturity assessment (Year 2) | 🔴 In Progress |
| `09-itil-assessment.md` | ITIL 4 service management assessment (Year 2) | 🔴 Planned |
| `year1-progress-report.md` | Full Year 1 progress report including incident timeline | ✅ Complete |

---

## Frameworks Applied

| Framework | Purpose | Status |
|---|---|---|
| **POPIA** (Protection of Personal Information Act, No. 4 of 2013) | Data protection compliance — 8 Conditions for Lawful Processing | Year 1 review complete |
| **SOC 2** — Trust Services Criteria (Security CC1–CC9 + Availability A1) | Security and availability controls readiness | Year 1 review complete |
| **COBIT 2019** | IT governance maturity assessment (Year 2) | In progress |
| **ITIL 4** | IT service management maturity assessment (Year 2) | Planned |

---

## Year 1 Risk Summary

| Metric | Month 0 | Month 12 |
|---|---|---|
| Total risks | 21 | 24 (+3 new) |
| High-rated risks | 8 | 1 |
| Medium-High risks | 13 | 8 |
| Closed risks | 0 | 8 |
| In Progress | 0 | 13 |
| Open (unresolved) | 21 | 3 |

---

## Year 1 Compliance Posture

| Framework | Month 0 | Month 12 |
|---|---|---|
| POPIA (8 conditions) | 0 compliant | 3 closed, 4 in progress, 1 open |
| SOC 2 Security (CC1–CC9) | 0 controls in place | 5 closed, 4 in progress |
| SOC 2 Availability (A1) | No SLA or monitoring | ✅ SLA live; 99.2% uptime |
| Incident Response | No plan | ✅ Plan tested in live incident |
| Vendor DPAs | 0 of 4 | 4 of 6 complete (Xero pending) |

---

## Methodology

Each finding follows a consistent five-part structure:
1. **Requirement summary** — what the framework requires, in plain English
2. **Current state** — what Khaya Payroll does (or did) today
3. **Gap identified** — the specific delta between requirement and reality
4. **Risk rating** — Low / Medium / Medium-High / High with explicit reasoning
5. **Recommendation** — specific, actionable fix

Annual reviews track each finding against its original rating and document progress, regression, or new risks that emerged during the year.

---

## Tools Used

- **draw.io / diagrams.net** — data flow diagramming
- **Notion** — GRC documentation and risk tracking
- **Microsoft Excel (.xlsx)** — risk register with traffic-light scoring
- **Markdown** — portable documentation for this repository
- **Nessus Essentials** — weekly vulnerability scanning (simulated)
- **UptimeRobot** — platform availability monitoring (simulated)
- **GitLab** — version control and change management log (simulated)

---

## Skills Demonstrated

- Regulatory gap assessment methodology (POPIA, SOC 2, COBIT, ITIL)
- Risk identification, rating, prioritization, and tracking over time
- Annual review and remediation progress reporting
- Security incident response and breach notification (POPIA s22)
- Data flow mapping and trust boundary analysis
- Vendor / third-party (sub-processor) risk assessment and DPA management
- Remediation roadmap planning with dependency sequencing
- Governance framework mapping (COBIT 2019, ITIL 4 — in progress)

---

## Project Status

🟡 **Year 1 complete. Year 2 (COBIT + ITIL assessment) in progress.**

---

*This is a self-directed portfolio project using a fictional company. It does not represent real client work or an actual audit engagement.*
