# 🗂️ Assets

> 6 systems in scope for GDPR compliance — the processing-activity inventory for EuroShop GmbH's EU e-commerce operations.

| # | Name | Type | Classification | Environment | Owner |
|---|---|---|---|---|---|
| 1 | Customer Master Database | Database | ![Critical](https://img.shields.io/badge/risk-Critical-b60205) | ![Production](https://img.shields.io/badge/env-Production-28a745) | Data Engineering Team |
| 2 | EuroShop E-Commerce Platform | Application | ![Critical](https://img.shields.io/badge/risk-Critical-b60205) | ![Production](https://img.shields.io/badge/env-Production-28a745) | Engineering Team |
| 3 | Marketing Analytics & CRM Platform | Application | ![High](https://img.shields.io/badge/risk-High-e36209) | ![Production](https://img.shields.io/badge/env-Production-28a745) | Marketing Team |
| 4 | Payment Gateway Integration | Cloud Account | ![Critical](https://img.shields.io/badge/risk-Critical-b60205) | ![Production](https://img.shields.io/badge/env-Production-28a745) | Payments Team |
| 5 | Customer Support & DSAR Ticketing System | Application | ![High](https://img.shields.io/badge/risk-High-e36209) | ![Production](https://img.shields.io/badge/env-Production-28a745) | Customer Support / Legal |
| 6 | Customer Data Warehouse | Data Store | ![High](https://img.shields.io/badge/risk-High-e36209) | ![Production](https://img.shields.io/badge/env-Production-28a745) | Data Engineering Team |

## 1. Customer Master Database

**Type:** Database &nbsp;·&nbsp; **Classification:** ![Critical](https://img.shields.io/badge/risk-Critical-b60205) &nbsp;·&nbsp; **Environment:** ![Production](https://img.shields.io/badge/env-Production-28a745)  
**Owner:** Data Engineering Team

**Description**  
Primary relational database holding personal data for 3M+ EU customers (names, addresses, contact details, order history, account credentials) across all 27 EU member states. Core subject of the GDPR processing-activity record (ROPA) and the system most DSARs will need to query against.

---

## 2. EuroShop E-Commerce Platform

**Type:** Application &nbsp;·&nbsp; **Classification:** ![Critical](https://img.shields.io/badge/risk-Critical-b60205) &nbsp;·&nbsp; **Environment:** ![Production](https://img.shields.io/badge/env-Production-28a745)  
**Owner:** Engineering Team

**Description**  
Customer-facing web and checkout application collecting personal data at account creation, checkout, and consent capture (cookie/marketing preferences) across all EU storefronts. Primary point of personal data collection and the main interface customers use to exercise GDPR rights (access, deletion, rectification).

---

## 3. Marketing Analytics & CRM Platform

**Type:** Application &nbsp;·&nbsp; **Classification:** ![High](https://img.shields.io/badge/risk-High-e36209) &nbsp;·&nbsp; **Environment:** ![Production](https://img.shields.io/badge/env-Production-28a745)  
**Owner:** Marketing Team

**Description**  
Customer relationship management and marketing analytics platform used for customer segmentation, behavioral tracking, and automated email/offer targeting. Performs profiling of customer purchase behavior, which brings it into scope for a GDPR Article 35 DPIA due to automated decision-making and large-scale profiling.

---

## 4. Payment Gateway Integration

**Type:** Cloud Account &nbsp;·&nbsp; **Classification:** ![Critical](https://img.shields.io/badge/risk-Critical-b60205) &nbsp;·&nbsp; **Environment:** ![Production](https://img.shields.io/badge/env-Production-28a745)  
**Owner:** Payments Team

**Description**  
Cloud account and API integration layer connecting EuroShop's checkout to third-party payment processors, handling payment and billing-address data for all EU transactions. Involves cross-border data transfer considerations and third-party processor due diligence under GDPR Article 28.

---

## 5. Customer Support & DSAR Ticketing System

**Type:** Application &nbsp;·&nbsp; **Classification:** ![High](https://img.shields.io/badge/risk-High-e36209) &nbsp;·&nbsp; **Environment:** ![Production](https://img.shields.io/badge/env-Production-28a745)  
**Owner:** Customer Support / Legal

**Description**  
Ticketing and case-management system used to log, track, and respond to customer inquiries, including Data Subject Access Requests (DSARs) for access, deletion, and rectification. Central system of record for demonstrating GDPR response-time compliance (one-month statutory deadline).

---

## 6. Customer Data Warehouse

**Type:** Data Store &nbsp;·&nbsp; **Classification:** ![High](https://img.shields.io/badge/risk-High-e36209) &nbsp;·&nbsp; **Environment:** ![Production](https://img.shields.io/badge/env-Production-28a745)  
**Owner:** Data Engineering Team

**Description**  
Aggregated analytics data store consolidating customer, order, and behavioral data from across all 27 EU markets for reporting and business intelligence. Holds large volumes of personal data at rest, including data replicated from multiple source systems, requiring its own entry in the data mapping and retention schedule.

---


---

<div align="center">

[← Overview](README.md) &nbsp;|&nbsp; [🏠 Home](README.md) &nbsp;|&nbsp; [Risk Register →](02-risk-register.md)

</div>
