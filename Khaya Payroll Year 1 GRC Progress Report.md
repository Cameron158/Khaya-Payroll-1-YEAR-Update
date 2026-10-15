# Khaya Payroll — Year 1 GRC Progress Report

**Assessment Period:** Month 1 – Month 12

| Document Control | |
|---|---|
| **Prepared by** | Information Officer (CEO) & Deputy Information Officer |
| **Review date** | Month 12 |
| **Next review** | Month 24 (annual) |
| **Document version** | 1.0 |
| **Status** | Final |

---

## 1. Executive Summary

This report summarises Khaya Payroll's compliance and security posture at the end of Year 1, measured against the remediation roadmap established in the original POPIA Gap Assessment and SOC 2 Gap Analysis. It serves as the baseline document for the Year 2 COBIT and ITIL framework assessments.

Khaya Payroll has made strong progress across Phase 1 (foundational) and Phase 2 (short-term) remediation activities, achieving full completion of Phase 1 and approximately 70% completion of Phase 2. The company experienced one reportable security incident in Month 7, which — while serious — validated the effectiveness of newly implemented controls and demonstrated that the incident response framework functioned as intended under real conditions.

The company has grown significantly over the year: from 180 to 256 clients, 35 to 54 staff, and from approximately 40,000 to 67,000 employee records processed monthly. This growth has introduced new risks (expanded attack surface, increased data volume, onboarding pace outstripping policy rollout) that will be addressed in the Year 2 assessment cycle.

> **Overall remediation status:** Phase 1 complete | Phase 2 ~70% complete | Phase 3 started

---

## 2. Company Growth — Year 1

| Metric | Start of Year 1 | End of Year 1 | Change |
|---|---|---|---|
| Active clients | 180 | 256 | +76 (+42%) |
| Staff headcount | 35 | 54 | +19 (+54%) |
| Employee records processed monthly | ~40,000 | ~67,000 | +27,000 (+68%) |
| Third-party sub-processors | 4 | 6 | +2 |

**Sub-processor detail:** SendGrid, Intercom, Payment Gateway, SARS eFiling, plus 2 new: Gusto payroll integration and Xero accounting API.

### Growth implications for Year 2

- The 6-month CC1 role review (scheduled per the original SOC 2 recommendation) is now due — Khaya Payroll's growth indicators (headcount, client volume) suggest the combined IO/security role is becoming stretched, and appointment of a dedicated Security Lead should be formally evaluated.
- Two new sub-processors (Gusto, Xero) were onboarded during the year; both have been added to the vendor register, though DPAs are still pending for one (Xero).
- Rapid staff growth (54% increase) has outpaced the security awareness training rollout — only 1 of 4 quarterly sessions was completed, meaning a significant portion of new staff have not yet received formal security training.

---

## 3. Security Incident — Month 7

### 3.1 Incident Summary

| Field | Detail |
|---|---|
| **Incident type** | Accidental data disclosure (human error) |
| **Incident date** | Month 7, Day 14 |
| **Reported by** | Client HR admin (Cape Town hospitality company) |
| **Affected data** | 43 employee payslips containing names, SA ID numbers, salary details, and banking information |
| **Number of unintended recipients** | 12 (other employees at the same company) |
| **Root cause** | Client HR admin used a bulk email distribution list incorrectly when distributing monthly payslips, sending to a broader group than intended |

### 3.2 Response Timeline

| Time | Action |
|---|---|
| T+0 hours | Client HR admin discovered the error and notified Khaya Payroll support via Intercom |
| T+1 hour | Support agent escalated to Deputy Information Officer per incident response plan |
| T+4 hours | IO activated incident response plan; incident formally declared and logged |
| T+6 hours | Affected data subjects (12 unintended recipients) contacted by client company, advised to disregard payslips received in error |
| T+48 hours | Internal investigation completed; root cause confirmed as client-side human error |
| T+68 hours | Information Regulator notified (within self-imposed 72-hour benchmark) |
| T+5 business days | Formal breach notification issued to 43 affected employees per POPIA s22 |
| T+30 days | Post-incident review completed; privacy notice template updated; client HR admin bulk-email guidance issued |

### 3.3 Findings from Incident

**What worked:**

- Incident response plan activated successfully within 4 hours of notification
- 72-hour notification benchmark met (68 hours)
- Escalation path from support → Deputy IO → IO functioned as designed
- Incident log maintained throughout with timestamps

**What didn't work:**

- No client-side training or guidance existed for HR admins on bulk email handling — this was a gap in the privacy notice template and operator guidance
- The device encryption gap (noted in the original assessment) was not relevant to this incident, but was highlighted as a risk that could have amplified the impact if a device had been involved
- The data subject notification template had not been pre-drafted — it was created reactively during the incident, adding approximately 8 hours to the notification timeline

**Remediation triggered by incident:**

- Privacy notice template updated to include bulk email handling guidance for HR admins
- Data subject notification template drafted and approved for future use
- Client onboarding checklist updated to include HR admin data handling training
- Tabletop exercise (Month 9) redesigned to include an accidental-disclosure scenario alongside the originally planned ransomware scenario

### 3.4 Regulatory Outcome

The Information Regulator acknowledged receipt of the breach notification. No enforcement action was taken, citing Khaya Payroll's prompt notification (within 72 hours), documented response, and proactive remediation steps. The Regulator noted the incident as consistent with "operator acting in good faith" under POPIA s21.

---

## 4. Phase 1 Remediation — Complete

All Phase 1 (Foundational, 0–30 days) items were completed by Month 2.

| Item | Status | Notes |
|---|---|---|
| POPIA Condition 1: IO registered with Information Regulator | ✅ Complete | CEO registered as IO (Month 1) |
| POPIA Condition 1: Deputy IO appointed | ✅ Complete | Head of Customer Success appointed as Deputy IO (Month 1) |
| SOC 2 CC1: IO mandate extended to include security oversight | ✅ Complete | Documented in IO appointment letter (Month 1) |
| SOC 2 CC2: security@ email and responsible disclosure policy | ✅ Complete | Live at security@khayapayroll.co.za (Month 2) |
| SOC 2 CC6: RBAC structure documented, access tiers defined | ✅ Complete | 3-tier access model documented (Month 2) |
| SOC 2 CC7: Incident response plan drafted and CEO-approved | ✅ Complete | IRP v1.0 approved (Month 2); tested in Month 7 incident |
| SOC 2 CC8: Git/GitLab implemented as change log | ✅ Complete | All repos migrated to GitLab (Month 2) |
| SOC 2 CC8: RFC template drafted | ✅ Complete | RFC template v1.0 approved (Month 2) |
| SOC 2 CC9: Vendor register built | ✅ Complete | 4 existing vendors documented (Month 2) |

---

## 5. Phase 2 Remediation — 70% Complete

### 5.1 Completed (Month 2–12)

| Item | Status | Notes |
|---|---|---|
| CC5: CEO-approved policy template established | ✅ Complete | Template v1.0 approved (Month 3) |
| CC5: Access Control Policy drafted and approved | ✅ Complete | ACP v1.0 approved (Month 3) |
| CC5: Incident Response Policy drafted and approved | ✅ Complete | IRP v1.0 approved (Month 2); used in Month 7 incident |
| CC6 / Condition 7: MFA implemented for all staff logins | ✅ Complete | MFA enforced for 100% of staff (Month 4) |
| CC7: Weekly Nessus Essentials vulnerability scans | ✅ Complete | Running since Month 3; 3 medium findings remediated |
| CC7: First tabletop exercise completed | ✅ Complete | Month 9; ransomware + accidental-disclosure scenarios |
| CC8: RFC approval process enforced | ✅ Complete | All changes require RFC since Month 3 |
| CC9: Infrastructure redundancy/failover implemented | ✅ Complete | Failover system live (Month 6) |
| A1: UptimeRobot monitoring live | ✅ Complete | 99.2% uptime achieved vs 99% SLA target |
| A1: SLA published in client contracts | ✅ Complete | Included in all new client contracts since Month 3 |

### 5.2 In Progress / Not Yet Complete

| Item | Status | Notes |
|---|---|---|
| CC6 / Condition 7: RBAC fully implemented | 🟡 60% complete | 3-tier model defined; technical implementation 60% migrated |
| CC6 / Condition 7: Encryption at rest confirmed | 🟡 In progress | Encryption confirmed for ID numbers; banking fields in progress |
| CC6: Device offboarding procedure | 🟡 Drafted, inconsistent | Procedure drafted (Month 4); enforcement inconsistent for remote staff |
| CC9: Manual payroll fallback process | 🟡 Drafted, untested | Template built; not yet tested with a client dry-run |
| CC5: Vendor Management Policy | 🔴 Not started | Deferred to Month 13; vendor register covers interim need |
| Condition 6: ROPA | 🟡 Started | ~60% complete; medical/leave data section still being scoped |
| Condition 8: Data subject request form on portal | 🔴 Not built | Engineering capacity constraints; targeted for Month 14 |
| Condition 3: Retention policy enforcement | 🟡 Policy written | Technical enforcement (automated flags) not yet built |
| Condition 4: Xero DPA | 🔴 Pending | Xero onboarded Month 10; DPA under legal review |

---

## 6. Phase 3 Remediation — Started, Inconsistent

| Item | Planned cadence | Actual completion | Notes |
|---|---|---|---|
| Monthly risk check-ins | 12 sessions | 8 of 10 completed | 2 missed due to enterprise client onboarding crunch |
| Quarterly deep-dive risk reviews | 3 sessions | 2 of 3 completed | Q3 review missed; rescheduled to Month 13 |
| Quarterly security awareness training | 4 sessions | 1 of 4 completed | Month 4 session only; new staff largely untrained |
| UptimeRobot uptime monitoring | Ongoing | ✅ Consistent | 99.2% uptime logged |
| Vendor certificate renewals | 4 vendors | 2 of 4 renewed | SendGrid and Payment Gateway renewed; Intercom and Gusto pending |
| Capacity planning review | Annual | ✅ Completed Month 11 | Infrastructure assessed; upgrade recommended for Q1 Year 2 |

---

## 7. Risk Register Summary — Year 1 Changes

| Risk ID | Original Rating | Current Rating | Status | Notes |
|---|---|---|---|---|
| R-001 | High | Low | ✅ Closed | IO registered; Deputy IO appointed |
| R-002 | Medium-High | Medium | 🟡 In Progress | Medical data standard drafted; not yet enforced |
| R-003 | Medium-High | Low | ✅ Closed | Legal basis mapping document completed |
| R-004 | Medium-High | Low | ✅ Closed | Privacy notice template published and distributed |
| R-005 | Medium-High | Medium | 🟡 In Progress | Retention policy written; technical enforcement pending |
| R-006 | Medium-High | Low | ✅ Closed | DPAs signed with Intercom, SendGrid, Payment Gateway |
| R-007 | Medium-High | Medium | 🟡 In Progress | Update confirmation implemented for banking details; ID number still pending |
| R-008 | High | Medium | 🟡 In Progress | ROPA 60% complete; rights notice published on portal |
| R-009 | High | Medium | 🟡 In Progress | MFA complete; RBAC 60% migrated; encryption in progress |
| R-010 | High | Low | ✅ Closed | IRP drafted, approved, and tested in Month 7 incident |
| R-011 | High | High | 🔴 Open | Data subject request form not yet built |
| R-012 | High | Low | ✅ Closed | IO mandate extended to include security oversight |
| R-013 | Medium-High | Low | ✅ Closed | security@ live; responsible disclosure policy published |
| R-014 | Medium-High | Medium | 🟡 In Progress | Monthly/quarterly reviews started; 2 of 3 quarterly sessions completed |
| R-015 | Medium-High | Medium | 🟡 In Progress | Control checklist implemented; some gaps in consistency |
| R-016 | High | Low | ✅ Closed | Policy template approved; ACP and IRP formally adopted |
| R-017 | Medium-High | Medium | 🟡 In Progress | Device procedure drafted; enforcement inconsistent for remote staff |
| R-018 | High | Medium | 🟡 In Progress | Native alerting live; Nessus running; tabletop done |
| R-019 | High | Low | ✅ Closed | GitLab + RFC process enforced for all changes |
| R-020 | High | Medium | 🟡 In Progress | Vendor register live; failover implemented; manual fallback untested |
| R-021 | Medium-High | Low | ✅ Closed | SLA published; UptimeRobot live; capacity review done |
| R-022 (NEW) | — | Medium-High | 🔴 Open | Rapid staff growth (54%) outpacing security training rollout — significant portion of new staff untrained |
| R-023 (NEW) | — | Medium | 🟡 In Progress | Two new sub-processors (Gusto, Xero) onboarded; Xero DPA pending |
| R-024 (NEW) | — | Medium | 🟡 In Progress | Month 7 incident revealed gap in client HR admin bulk-email handling guidance; partially remediated |

---

## 8. New Risks Identified in Year 1

Three new risks emerged during Year 1 that were not present in the original assessment.

### R-022: Staff growth outpacing security training

The 54% headcount increase (35→54 staff) combined with only 1 of 4 quarterly training sessions being delivered means a significant proportion of new staff have not received formal security awareness training. This increases the likelihood of human-error incidents (similar to the Month 7 event) and reduces the effectiveness of controls that depend on staff awareness (phishing recognition, incident reporting).

### R-023: New sub-processor onboarding gap

Two new sub-processors (Gusto payroll integration, Xero accounting API) were onboarded during the year. Gusto's DPA was completed at onboarding; Xero's DPA is still under legal review at Month 12. The vendor register is updated, but the Xero gap represents an active POPIA Condition 4 / SOC 2 CC9 compliance gap.

### R-024: Client HR admin data handling gap

The Month 7 incident revealed that the original privacy notice template and client onboarding process did not include sufficient guidance on bulk data handling (e.g. bulk email distribution of payslips). This has been partially remediated (template updated, guidance issued) but has not been tested across all 256 clients.

---

## 9. Year 2 Priorities

Based on Year 1 outcomes, the following are the highest-priority items for the Year 2 assessment cycle.

### Immediate (Month 13–14)

1. Complete RBAC technical implementation (currently 60%)
2. Confirm encryption at rest on banking fields
3. Build data subject request form on self-service portal (R-011)
4. Complete Xero DPA (R-023)
5. Draft and approve Vendor Management Policy

### Short-term (Month 15–18)

6. Deliver remaining 3 quarterly security awareness training sessions (prioritise new staff)
7. Test manual payroll fallback process with a client dry-run
8. Complete ROPA (currently 60%)
9. Enforce device offboarding procedure for remote staff consistently

### Governance (ongoing)

10. Conduct 6-month CC1 role review — assess whether dedicated Security Lead is now warranted given 54% staff growth and 42% client growth
11. Apply COBIT 2019 governance framework to assess IT governance maturity
12. Apply ITIL 4 framework to assess service management maturity (Incident Management, Change Enablement, Service Level Management, Availability Management)

---

## 10. Overall Compliance Posture — Year 1 Scorecard

| Framework | Original Posture | Year 1 Posture | Trend |
|---|---|---|---|
| POPIA (8 Conditions) | Non-compliant across all 8 | Compliant: 3 \| Partially compliant: 4 \| Non-compliant: 1 | ↑ Significant improvement |
| SOC 2 Security (CC1–CC9) | No controls in place | Controls in place: 5 \| In progress: 4 \| Not started: 0 | ↑ Significant improvement |
| SOC 2 Availability (A1) | No SLA or monitoring | SLA live; 99.2% uptime | ↑ Complete |
| Incident Response | No plan | Plan tested in live incident | ↑ Complete |
| Vendor Management | No DPAs | 3 of 5 DPAs complete | ↑ Improving |

---

*This report is a simulated Year 1 progress update for a self-directed GRC portfolio project using a fictional company (Khaya Payroll Pty Ltd). It does not represent a real audit engagement or legal advice.*
