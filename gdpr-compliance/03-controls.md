# 🛡️ Controls

> 10 controls, primarily mapped to GDPR articles, addressing the risks above.

| # | Control | Framework | Reference | Effectiveness | Frequency |
|---|---|---|---|---|---|
| 1 | Role-Based Access Control with Least Privilege on Customer Database | ISO 27001 | `A.8.3` | ![Partially Effective](https://img.shields.io/badge/status-Partially%20Effective-dbab09) | Continuous |
| 2 | DSAR Intake and Tracking Workflow with Automated Deadline Alerts | GDPR | `Art. 12(3)` | ![Partially Effective](https://img.shields.io/badge/status-Partially%20Effective-dbab09) | Continuous |
| 3 | Automated Personal Data Discovery Tooling Across Customer Systems | GDPR | `Art. 15` | ![Not Tested](https://img.shields.io/badge/status-Not%20Tested-6a737d) | Continuous |
| 4 | Data Protection Impact Assessment Process for High-Risk Processing | GDPR | `Art. 35` | ![Not Tested](https://img.shields.io/badge/status-Not%20Tested-6a737d) | Annual |
| 5 | Automated Decision-Making and Profiling Opt-Out Mechanism | GDPR | `Art. 22` | ![Partially Effective](https://img.shields.io/badge/status-Partially%20Effective-dbab09) | Continuous |
| 6 | Standard Contractual Clauses with Payment Processor | GDPR | `Art. 46(2)(c)` | ![Not Tested](https://img.shields.io/badge/status-Not%20Tested-6a737d) | Annual |
| 7 | Vendor Data Processing Agreement and Due Diligence Review | GDPR | `Art. 28` | ![Partially Effective](https://img.shields.io/badge/status-Partially%20Effective-dbab09) | Annual |
| 8 | Requester Identity Verification Procedure for DSAR Fulfillment | GDPR | `Art. 12(6)` | ![Not Tested](https://img.shields.io/badge/status-Not%20Tested-6a737d) | Continuous |
| 9 | Data Retention and Automated Deletion Schedule for Data Warehouse | GDPR | `Art. 5(1)(e)` | ![Not Tested](https://img.shields.io/badge/status-Not%20Tested-6a737d) | Quarterly |
| 10 | Breach Notification Runbook and 72-Hour Reporting Procedure | GDPR | `Art. 33` | ![Not Tested](https://img.shields.io/badge/status-Not%20Tested-6a737d) | Annual |

## 1. Role-Based Access Control with Least Privilege on Customer Database

**Framework:** ISO 27001 `A.8.3` &nbsp;·&nbsp; **Frequency:** Continuous  
**Effectiveness:** ![Partially Effective](https://img.shields.io/badge/status-Partially%20Effective-dbab09) &nbsp;·&nbsp; **Owner:** Data Engineering Team

**Description**  
Restrict Customer Master Database access to named roles (support-read, analytics-read, engineering-admin) rather than broad default access, provisioned and reviewed through the identity access management system. Enforced via database-level role grants tied to Active Directory group membership.

**Decision Rationale**  
Rated Partially Effective because roles exist and are enforced technically, but the most recent access review found several roles granted broader read access than their function requires (e.g. analytics roles with write access), matching the overly permissive access gap identified in the related risk. Tightening is in progress but not yet complete.

---

## 2. DSAR Intake and Tracking Workflow with Automated Deadline Alerts

**Framework:** GDPR `Art. 12(3)` &nbsp;·&nbsp; **Frequency:** Continuous  
**Effectiveness:** ![Partially Effective](https://img.shields.io/badge/status-Partially%20Effective-dbab09) &nbsp;·&nbsp; **Owner:** Customer Support / Legal

**Description**  
Log every Data Subject Access Request in the DSAR Ticketing System at intake, with the statutory one-month response deadline calculated automatically and escalation alerts sent to the case owner at 2 weeks, 1 week, and 2 days before the deadline.

**Decision Rationale**  
Rated Partially Effective because the intake workflow and deadline field are in place and used for every request, but the automated escalation alerts are not yet live — deadline tracking today still depends on the case owner checking manually, which is the same gap the related risk identifies.

---

## 3. Automated Personal Data Discovery Tooling Across Customer Systems

**Framework:** GDPR `Art. 15` &nbsp;·&nbsp; **Frequency:** Continuous  
**Effectiveness:** ![Not Tested](https://img.shields.io/badge/status-Not%20Tested-6a737d) &nbsp;·&nbsp; **Owner:** Data Engineering Team

**Description**  
Deploy a data-discovery tool that, given a customer identifier, queries the Customer Master Database, Data Warehouse, and Marketing/CRM platform to return every location holding that customer's personal data, to speed up DSAR fulfillment.

**Decision Rationale**  
Rated Not Tested because the tool is in pilot against a single system (the Customer Master Database) and has not yet been validated against the Data Warehouse or Marketing/CRM platform, so it cannot yet be relied on to return a complete picture of a customer's data for a DSAR.

---

## 4. Data Protection Impact Assessment Process for High-Risk Processing

**Framework:** GDPR `Art. 35` &nbsp;·&nbsp; **Frequency:** Annual  
**Effectiveness:** ![Not Tested](https://img.shields.io/badge/status-Not%20Tested-6a737d) &nbsp;·&nbsp; **Owner:** Marketing Team

**Description**  
Require a documented DPIA — describing the processing, necessity and proportionality, and risk mitigation measures — before any new high-risk processing activity (including profiling) goes live, reviewed and signed off by the DPO.

**Decision Rationale**  
Rated Not Tested because the DPIA template and process have been drafted but not yet applied to a real assessment; the Marketing Analytics & CRM Platform's existing profiling activity predates this process and has not yet been retroactively assessed, which is the exact gap the related risk describes.

---

## 5. Automated Decision-Making and Profiling Opt-Out Mechanism

**Framework:** GDPR `Art. 22` &nbsp;·&nbsp; **Frequency:** Continuous  
**Effectiveness:** ![Partially Effective](https://img.shields.io/badge/status-Partially%20Effective-dbab09) &nbsp;·&nbsp; **Owner:** Marketing Team

**Description**  
Provide customers a clear, accessible control in account settings to opt out of behavioral profiling and automated offer targeting, with opt-out honored within 24 hours across the Marketing Analytics & CRM Platform.

**Decision Rationale**  
Rated Partially Effective because the opt-out mechanism exists and functions technically, but it is currently buried three menus deep in account settings rather than surfaced at the point profiling is first used, which falls short of the 'clear and accessible' standard the control is meant to meet.

---

## 6. Standard Contractual Clauses with Payment Processor

**Framework:** GDPR `Art. 46(2)(c)` &nbsp;·&nbsp; **Frequency:** Annual  
**Effectiveness:** ![Not Tested](https://img.shields.io/badge/status-Not%20Tested-6a737d) &nbsp;·&nbsp; **Owner:** Payments Team

**Description**  
Confirm and file a signed, current set of Standard Contractual Clauses (or equivalent Article 46 transfer mechanism) with the third-party payment processor covering all EU customer payment data transferred outside the EEA.

**Decision Rationale**  
Rated Not Tested because the current SCC documentation status with the payment processor has not yet been confirmed — legal has requested the signed agreement but it has not been received and verified, so the transfer mechanism's validity cannot yet be confirmed.

---

## 7. Vendor Data Processing Agreement and Due Diligence Review

**Framework:** GDPR `Art. 28` &nbsp;·&nbsp; **Frequency:** Annual  
**Effectiveness:** ![Partially Effective](https://img.shields.io/badge/status-Partially%20Effective-dbab09) &nbsp;·&nbsp; **Owner:** Payments Team

**Description**  
Maintain a signed Data Processing Agreement with every third-party processor handling EU customer data, with an annual due-diligence review covering their security controls, sub-processor list, and breach notification commitments.

**Decision Rationale**  
Rated Partially Effective because a signed DPA is on file for the payment processor, but the annual due-diligence review has not been formalized as a recurring process — the last review was ad hoc rather than scheduled, so ongoing assurance isn't guaranteed going forward.

---

## 8. Requester Identity Verification Procedure for DSAR Fulfillment

**Framework:** GDPR `Art. 12(6)` &nbsp;·&nbsp; **Frequency:** Continuous  
**Effectiveness:** ![Not Tested](https://img.shields.io/badge/status-Not%20Tested-6a737d) &nbsp;·&nbsp; **Owner:** Customer Support / Legal

**Description**  
Require support agents to verify a requester's identity (matching account email plus one additional identifier, e.g. order number or postal code) before releasing any personal data in response to a DSAR, documented on the ticket.

**Decision Rationale**  
Rated Not Tested because the verification procedure has been written and distributed to the support team, but no completed DSAR has yet been fulfilled under it, so whether agents consistently follow it in practice has not been confirmed.

---

## 9. Data Retention and Automated Deletion Schedule for Data Warehouse

**Framework:** GDPR `Art. 5(1)(e)` &nbsp;·&nbsp; **Frequency:** Quarterly  
**Effectiveness:** ![Not Tested](https://img.shields.io/badge/status-Not%20Tested-6a737d) &nbsp;·&nbsp; **Owner:** Data Engineering Team

**Description**  
Define a maximum retention period per data category in the Customer Data Warehouse (e.g. order history, browsing behavior, marketing consent records) and enforce it with an automated deletion or archiving job reviewed quarterly.

**Decision Rationale**  
Rated Not Tested because the retention schedule has been drafted and approved, but the automated deletion job has not yet been built or run, so no personal data has actually been deleted under this control yet — it exists on paper only at this point.

---

## 10. Breach Notification Runbook and 72-Hour Reporting Procedure

**Framework:** GDPR `Art. 33` &nbsp;·&nbsp; **Frequency:** Annual  
**Effectiveness:** ![Not Tested](https://img.shields.io/badge/status-Not%20Tested-6a737d) &nbsp;·&nbsp; **Owner:** Data Engineering Team

**Description**  
Maintain a documented incident-response runbook that walks the team through assessing, containing, and reporting a personal data breach to the relevant supervisory authority within 72 hours of becoming aware, with a pre-built notification template per EU member state requirement.

**Decision Rationale**  
Rated Not Tested because the runbook has been written but has not yet been exercised through a tabletop simulation, so the team's actual ability to meet the 72-hour window under real conditions — including identifying the correct lead supervisory authority across 27 member states — remains unconfirmed.

---


---

<div align="center">

[← Risk Register](02-risk-register.md) &nbsp;|&nbsp; [🏠 Home](README.md) &nbsp;|&nbsp; [Evidence →](04-evidence.md)

</div>
