# ⚠️ Risk Register

> 6 risks, each written as [Threat] exploits [Vulnerability] causing [Impact] to [Asset].

| # | Title | Category | Status | Risk Score |
|---|---|---|---|---|
| 1 | External attacker exploits overly permissive access controls causing unauthorized access to Customer Master Database | Access Control | ![Open](https://img.shields.io/badge/status-Open-d73a49) | 15 (3 × 5) — Critical |
| 2 | Rising DSAR volume exploits lack of automated data-discovery tooling causing missed response deadlines on the E-Commerce Platform | Compliance | ![In Progress](https://img.shields.io/badge/status-In%20Progress-dbab09) | 12 (4 × 3) — High |
| 3 | Automated profiling exploits absence of a completed DPIA causing non-compliant processing on the Marketing Analytics & CRM Platform | Compliance | ![In Progress](https://img.shields.io/badge/status-In%20Progress-dbab09) | 16 (4 × 4) — Critical |
| 4 | Cross-border payment processing exploits missing Standard Contractual Clauses causing unlawful data transfer via the Payment Gateway Integration | Vendor Risk | ![Open](https://img.shields.io/badge/status-Open-d73a49) | 15 (3 × 5) — Critical |
| 5 | Support agent exploits absent identity-verification procedure causing wrongful disclosure of personal data via the DSAR Ticketing System | Human Error | ![Open](https://img.shields.io/badge/status-Open-d73a49) | 12 (3 × 4) — High |
| 6 | Absence of a retention policy exploits lack of automated deletion rules causing indefinite data storage in the Customer Data Warehouse | Data Protection | ![Open](https://img.shields.io/badge/status-Open-d73a49) | 12 (4 × 3) — High |

## 1. External attacker exploits overly permissive access controls causing unauthorized access to Customer Master Database

**Category:** Access Control &nbsp;·&nbsp; **Status:** ![Open](https://img.shields.io/badge/status-Open-d73a49)  
**Likelihood:** 3/5 &nbsp;·&nbsp; **Impact:** 5/5 &nbsp;·&nbsp; **Risk Score:** 15 (3 × 5) — Critical  
**Owner:** Data Engineering Team

**Description**  
An external attacker exploits broad or poorly scoped database access permissions to gain unauthorized access to the Customer Master Database, exposing personal data for 3M+ EU customers across all 27 member states.

**Decision Rationale**  
Likelihood rated Possible (3) because the database is a high-value target for attackers but no specific exploited vulnerability or prior incident has been confirmed. Impact rated Severe (5) because a breach at this scale triggers mandatory GDPR breach notification to supervisory authorities in multiple member states within 72 hours, individual notification obligations, and exposure to fines of up to 4% of global annual turnover.

---

## 2. Rising DSAR volume exploits lack of automated data-discovery tooling causing missed response deadlines on the E-Commerce Platform

**Category:** Compliance &nbsp;·&nbsp; **Status:** ![In Progress](https://img.shields.io/badge/status-In%20Progress-dbab09)  
**Likelihood:** 4/5 &nbsp;·&nbsp; **Impact:** 3/5 &nbsp;·&nbsp; **Risk Score:** 12 (4 × 3) — High  
**Owner:** Customer Support / Legal

**Description**  
As DSAR volume grows with the customer base, the absence of automated tooling to locate a given customer's personal data across the E-Commerce Platform causes manual, slow fulfillment that risks missing the GDPR Article 12 one-month statutory response deadline.

**Decision Rationale**  
Likelihood rated Likely (4) because DSAR volume scales directly with the 3M+ customer base and the process today is manual. Impact rated Moderate (3) because individual missed deadlines typically result in a regulatory warning or complaint-driven inquiry rather than an immediate fine, though repeated or systemic misses would escalate enforcement risk.

---

## 3. Automated profiling exploits absence of a completed DPIA causing non-compliant processing on the Marketing Analytics & CRM Platform

**Category:** Compliance &nbsp;·&nbsp; **Status:** ![In Progress](https://img.shields.io/badge/status-In%20Progress-dbab09)  
**Likelihood:** 4/5 &nbsp;·&nbsp; **Impact:** 4/5 &nbsp;·&nbsp; **Risk Score:** 16 (4 × 4) — Critical  
**Owner:** Marketing Team

**Description**  
The Marketing Analytics & CRM Platform performs automated profiling of customer purchase behavior for targeting purposes without a completed Data Protection Impact Assessment, exploiting the governance gap to continue processing that GDPR Article 35 requires to be assessed before it begins.

**Decision Rationale**  
Likelihood rated Likely (4) because the profiling activity is already running today without a DPIA — this is an active gap, not a hypothetical one. Impact rated Major (4) because large-scale profiling without a required DPIA is a direct Article 35 violation that a supervisory authority could act on, though impact is bounded by the fact that no unlawful processing of special-category data is currently indicated.

---

## 4. Cross-border payment processing exploits missing Standard Contractual Clauses causing unlawful data transfer via the Payment Gateway Integration

**Category:** Vendor Risk &nbsp;·&nbsp; **Status:** ![Open](https://img.shields.io/badge/status-Open-d73a49)  
**Likelihood:** 3/5 &nbsp;·&nbsp; **Impact:** 5/5 &nbsp;·&nbsp; **Risk Score:** 15 (3 × 5) — Critical  
**Owner:** Payments Team

**Description**  
Payment and billing data for EU customers is transferred to a third-party payment processor without confirmed Standard Contractual Clauses or an equivalent GDPR Chapter V transfer mechanism in place, exploiting the contractual gap to create an unlawful international data transfer.

**Decision Rationale**  
Likelihood rated Possible (3) pending confirmation of the processor's current transfer documentation status. Impact rated Severe (5) because an invalid transfer mechanism can force suspension of the data flow entirely (halting payment processing), carries some of the highest GDPR fines on record industry-wide, and directly affects all EU transactions, not a subset of customers.

---

## 5. Support agent exploits absent identity-verification procedure causing wrongful disclosure of personal data via the DSAR Ticketing System

**Category:** Human Error &nbsp;·&nbsp; **Status:** ![Open](https://img.shields.io/badge/status-Open-d73a49)  
**Likelihood:** 3/5 &nbsp;·&nbsp; **Impact:** 4/5 &nbsp;·&nbsp; **Risk Score:** 12 (3 × 4) — High  
**Owner:** Customer Support / Legal

**Description**  
Without a standardized procedure to verify a requester's identity before fulfilling a Data Subject Access Request, a support agent exploits the gap and discloses another customer's personal data to the wrong individual through the DSAR Ticketing System.

**Decision Rationale**  
Likelihood rated Possible (3) because identity verification failures are a recognized, recurring failure mode in DSAR handling across the industry, especially under response-time pressure. Impact rated Major (4) because a wrongful disclosure is itself a reportable personal data breach, compounding the harm it was meant to prevent.

---

## 6. Absence of a retention policy exploits lack of automated deletion rules causing indefinite data storage in the Customer Data Warehouse

**Category:** Data Protection &nbsp;·&nbsp; **Status:** ![Open](https://img.shields.io/badge/status-Open-d73a49)  
**Likelihood:** 4/5 &nbsp;·&nbsp; **Impact:** 3/5 &nbsp;·&nbsp; **Risk Score:** 12 (4 × 3) — High  
**Owner:** Data Engineering Team

**Description**  
Without a defined and enforced data retention schedule, the Customer Data Warehouse exploits the lack of automated deletion or archiving rules to retain customer personal data indefinitely, beyond the purpose for which it was originally collected.

**Decision Rationale**  
Likelihood rated Likely (4) because data warehouses commonly accumulate data by default before a retention program matures, and no deletion automation currently exists. Impact rated Moderate (3) because indefinite retention is a clear violation of the GDPR storage limitation principle, but on its own (absent a breach or a specific complaint) is less likely to trigger immediate severe enforcement compared to an unlawful transfer or unauthorized access event.

---


---

<div align="center">

[← Assets](01-assets.md) &nbsp;|&nbsp; [🏠 Home](README.md) &nbsp;|&nbsp; [Controls →](03-controls.md)

</div>
