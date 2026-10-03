# 📎 Evidence

> 10 evidence artifacts, one per control, documenting current implementation state — not all of them a clean pass.

| # | Title | Type | Related Control | Owner |
|---|---|---|---|---|
| 1 | Database Role Grant Export — Customer Master Database | Export | CTL-museds9a — Role-Based Access Control with Least Privilege on Customer Database | Data Engineering Team |
| 2 | DSAR Ticketing System Workflow Configuration Screenshot | Screenshot | CTL-museg3rn — DSAR Intake and Tracking Workflow with Automated Deadline Alerts | Customer Support / Legal |
| 3 | Data Discovery Pilot Test Report — Customer Master Database | Report | CTL-musehobb — Automated Personal Data Discovery Tooling Across Customer Systems | Data Engineering Team |
| 4 | DPIA Template and Process Document (Draft) | Document | CTL-museivr2 — Data Protection Impact Assessment Process for High-Risk Processing | Marketing Team |
| 5 | Profiling Opt-Out Setting — Account Settings Screenshot | Screenshot | CTL-musejjgi — Automated Decision-Making and Profiling Opt-Out Mechanism | Marketing Team |
| 6 | Payment Processor Data Transfer Agreement Status — Email Confirmation | Document | CTL-musemnme — Standard Contractual Clauses with Payment Processor | Payments Team |
| 7 | Signed Data Processing Agreement — Payment Processor | Document | CTL-musenpvm — Vendor Data Processing Agreement and Due Diligence Review | Payments Team |
| 8 | DSAR Identity Verification Procedure Document | Document | CTL-museouk2 — Requester Identity Verification Procedure for DSAR Fulfillment | Customer Support / Legal |
| 9 | Data Retention Schedule — Approved Policy Document | Document | CTL-musept4m — Data Retention and Automated Deletion Schedule for Data Warehouse | Data Engineering Team |
| 10 | Breach Notification Runbook Document | Document | CTL-museskyg — Breach Notification Runbook and 72-Hour Reporting Procedure | Data Engineering Team |

## 1. Database Role Grant Export — Customer Master Database

**Type:** Export &nbsp;·&nbsp; **Owner:** Data Engineering Team  
**Related Control:** CTL-museds9a — Role-Based Access Control with Least Privilege on Customer Database  
**Location:** `Evidence Repository / GDPR / Art32-RBAC / db-role-grants-export.csv`

**Notes**  
Export listing every database role and its granted permissions; used to confirm which roles have broader access than their function requires — the specific gap behind this control's Partially Effective rating.

---

## 2. DSAR Ticketing System Workflow Configuration Screenshot

**Type:** Screenshot &nbsp;·&nbsp; **Owner:** Customer Support / Legal  
**Related Control:** CTL-museg3rn — DSAR Intake and Tracking Workflow with Automated Deadline Alerts  
**Location:** `Evidence Repository / GDPR / Art12-DSAR / dsar-workflow-config-screenshot.png`

**Notes**  
Shows the intake form and automatic one-month deadline field. Escalation alert rules are not yet visible in this configuration, consistent with alerts not being live yet.

---

## 3. Data Discovery Pilot Test Report — Customer Master Database

**Type:** Report &nbsp;·&nbsp; **Owner:** Data Engineering Team  
**Related Control:** CTL-musehobb — Automated Personal Data Discovery Tooling Across Customer Systems  
**Location:** `Evidence Repository / GDPR / Art15-Discovery / data-discovery-pilot-report.pdf`

**Notes**  
Pilot test report covering lookups against the Customer Master Database only; documents that Data Warehouse and Marketing/CRM coverage is not yet included, so results are not yet a complete picture for a DSAR.

---

## 4. DPIA Template and Process Document (Draft)

**Type:** Document &nbsp;·&nbsp; **Owner:** Marketing Team  
**Related Control:** CTL-museivr2 — Data Protection Impact Assessment Process for High-Risk Processing  
**Location:** `Evidence Repository / GDPR / Art35-DPIA / dpia-template-process-draft.docx`

**Notes**  
Draft DPIA template and DPO sign-off workflow. No completed DPIA has been filed against it yet, including none for the Marketing/CRM profiling activity already in production.

---

## 5. Profiling Opt-Out Setting — Account Settings Screenshot

**Type:** Screenshot &nbsp;·&nbsp; **Owner:** Marketing Team  
**Related Control:** CTL-musejjgi — Automated Decision-Making and Profiling Opt-Out Mechanism  
**Location:** `Evidence Repository / GDPR / Art22-OptOut / profiling-optout-screenshot.png`

**Notes**  
Shows the opt-out toggle located under Settings > Privacy > Advanced — supports the finding that it is functional but not surfaced clearly at the point profiling is first used.

---

## 6. Payment Processor Data Transfer Agreement Status — Email Confirmation

**Type:** Document &nbsp;·&nbsp; **Owner:** Payments Team  
**Related Control:** CTL-musemnme — Standard Contractual Clauses with Payment Processor  
**Location:** `Evidence Repository / GDPR / Art46-SCC / processor-sccs-status-email.pdf`

**Notes**  
Correspondence with the payment processor's legal team requesting a current signed SCC copy. As of this evidence, the signed document has not yet been received or verified.

---

## 7. Signed Data Processing Agreement — Payment Processor

**Type:** Document &nbsp;·&nbsp; **Owner:** Payments Team  
**Related Control:** CTL-musenpvm — Vendor Data Processing Agreement and Due Diligence Review  
**Location:** `Evidence Repository / GDPR / Art28-DPA / payment-processor-dpa-signed.pdf`

**Notes**  
Signed DPA on file covering the payment processor. No corresponding scheduled due-diligence review record exists yet, which is the gap behind this control's Partially Effective rating.

---

## 8. DSAR Identity Verification Procedure Document

**Type:** Document &nbsp;·&nbsp; **Owner:** Customer Support / Legal  
**Related Control:** CTL-museouk2 — Requester Identity Verification Procedure for DSAR Fulfillment  
**Location:** `Evidence Repository / GDPR / Art12-Verification / dsar-identity-verification-procedure.docx`

**Notes**  
Written verification procedure distributed to the support team. No completed DSAR case log yet demonstrates the procedure being followed in practice.

---

## 9. Data Retention Schedule — Approved Policy Document

**Type:** Document &nbsp;·&nbsp; **Owner:** Data Engineering Team  
**Related Control:** CTL-musept4m — Data Retention and Automated Deletion Schedule for Data Warehouse  
**Location:** `Evidence Repository / GDPR / Art5-Retention / data-retention-schedule-approved.pdf`

**Notes**  
Approved retention periods by data category for the Data Warehouse. The automated deletion job implementing this schedule has not yet been built, so no deletion log exists yet.

---

## 10. Breach Notification Runbook Document

**Type:** Document &nbsp;·&nbsp; **Owner:** Data Engineering Team  
**Related Control:** CTL-museskyg — Breach Notification Runbook and 72-Hour Reporting Procedure  
**Location:** `Evidence Repository / GDPR / Art33-Breach / breach-notification-runbook.docx`

**Notes**  
Documented runbook and per-member-state notification templates. No tabletop exercise has yet been run to validate it under simulated conditions.

---


---

<div align="center">

[← Controls](03-controls.md) &nbsp;|&nbsp; [🏠 Home](README.md) &nbsp;|&nbsp; [Policies →](05-policies.md)

</div>
