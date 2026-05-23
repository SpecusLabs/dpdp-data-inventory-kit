# D2C E-Commerce — Data Flow Guide

**By Specus Labs**

---

> **Disclaimer:** This document is for informational purposes only. It does not constitute legal advice. Consult a qualified legal professional for advice specific to your organisation.

---

## Overview

A typical D2C (direct-to-consumer) e-commerce business running on platforms like Shopify or WooCommerce will handle personal data across 6–12 systems. Most founders, when they map this for the first time, are surprised by how many systems carry customer data.

This guide walks through how data typically flows in a D2C business, what the DPDP Act requires at each stage, and what actions to take.

---

## Data entry points

### 1. Product checkout
**Data collected:** Customer name, email address, mobile number, delivery address, pin code, payment method details.

**DPDP obligation:** Consent is required before or at the point of collection (Section 6). Your checkout page must display a link to your privacy policy and a consent mechanism. Pre-ticked boxes do not constitute valid consent.

**Common gap:** Most Shopify stores have no explicit consent checkbox at checkout. The privacy policy link alone is generally insufficient under the DPDP Act.

**Action:** Add a consent checkbox at checkout that links to your privacy policy. Record the timestamp of consent.

### 2. Account registration
**Data collected:** Name, email, password (hashed), mobile number, date of birth (optional), marketing preferences.

**DPDP obligation:** Consent required (Section 6). Marketing preferences must be separate from account creation — a customer should be able to create an account without agreeing to marketing emails.

### 3. Email/WhatsApp newsletter sign-up
**Data collected:** Email address or mobile number, name (optional).

**DPDP obligation:** Separate, explicit consent required for marketing communications. The purpose must be clearly stated at sign-up.

### 4. Social media ad click-through
**Data collected:** The ad platform (Meta, Google) passes attribution data. Your website's tracking pixel collects device identifiers and session behaviour.

**DPDP obligation:** Requires disclosure in privacy policy. Meta's custom audience upload (hashed email/phone) also requires consent from the customer.

### 5. Customer support contact
**Data collected:** Name, email or phone, query details, potentially order details or delivery complaints.

**DPDP obligation:** Support data is personal data. It must have a retention period and be accessible/eraseable on request.

---

## Data storage locations

| System | Data Stored | Key Risk |
|---|---|---|
| Shopify | Customer profiles, orders, addresses, notes | Vendor DPA needed |
| Payment gateway (Razorpay / PayU / Cashfree) | Transaction records, tokenised payment data | Regulatory retention requirements |
| Email marketing tool (Klaviyo / Mailchimp / WebEngage) | Email lists, campaign engagement | Unsubscribe processing must be immediate |
| Logistics platform (Shiprocket / Pickrr / EasyEcom) | Name, phone, address, order details | Sub-processors used by these platforms |
| Customer support tool (Intercom / Freshdesk / Zendesk) | Support conversations, issue history | Often overlooked in inventory |
| Analytics (GA4, Hotjar, Mixpanel) | Session data, behavioural data | Needs cookie consent; children's data risk |
| Meta Ads / Google Ads | Custom audience data, ad engagement | Cross-border transfer; requires disclosure |
| Internal spreadsheets or databases | Ad hoc customer data, VIP lists | Highest risk — often uncontrolled access |

---

## Data flows to third parties

**Logistics vendors**
When an order is placed, customer name, phone, and delivery address are automatically sent to Shiprocket or similar platforms. These platforms then share this data with last-mile carriers (Delhivery, Ekart, DTDC). Each of these is a Data Processor.

**Action:** Issue DPAs to your logistics platform. Confirm that their contracts with sub-processors include data protection terms.

**Email marketing platforms**
Customer purchase history and email addresses are synced from Shopify to Klaviyo (or equivalent). This creates a detailed customer profile in a US-based SaaS platform.

**Action:** Issue DPA with Klaviyo. Disclose cross-border transfer in privacy policy.

**Payment gateways**
Payment data is processed by Razorpay or equivalent and is subject to RBI regulations. These platforms maintain their own regulatory compliance.

**Action:** Confirm DPA is signed. Note that payment records cannot be deleted due to regulatory requirements — document this exception in your inventory.

**Meta and Google ad platforms**
Customer email addresses and phone numbers are uploaded (hashed) as custom audiences. Ad engagement data is collected via pixels.

**Action:** Require explicit consent before uploading custom audiences. Disclose in privacy policy.

---

## Data deletion obligations

Under Section 8(7) of the DPDP Act, personal data must be deleted when it is no longer needed for the stated purpose.

**Recommended retention periods for D2C:**

| Data Category | Suggested Retention | Reason |
|---|---|---|
| Customer purchase records | 3–5 years from last order | Consumer protection and warranty obligations |
| Payment transaction records | 5–8 years | RBI and GST compliance |
| Marketing email list (active) | Until unsubscribe or opt-out | No time limit — but delete promptly on opt-out |
| Marketing email list (inactive — no engagement in 12 months) | 12–18 months | Minimal purpose after extended inactivity |
| Guest checkout data (no account) | 2 years from order date | Balance of operational need and minimisation |
| Support conversation records | 2–3 years from resolution | Sufficient for disputes and warranty |
| Analytics / behavioural data | 26 months (GA4 default) or less | No ongoing purpose beyond analytics window |

---

## DPDP Act checklist for D2C businesses

- [ ] Consent checkbox at checkout with privacy policy link (Section 6)
- [ ] Separate opt-in for marketing emails / WhatsApp messages
- [ ] Privacy policy published and accurate — reflects actual systems used
- [ ] DPA in place with: Razorpay / payment gateway, Shiprocket / logistics platform, email marketing platform
- [ ] Cookie consent banner implemented for GA4 and Meta Pixel
- [ ] Customer erasure request process documented (Section 12)
- [ ] Customer access request process documented (Section 11)
- [ ] Retention periods set and deletion schedule created
- [ ] HR data (if applicable) stored securely with restricted access
- [ ] Children's data flag — if you sell products for children, parental consent mechanism required (Section 9)

---

*Built by [Specus Labs](https://github.com/specuslabs) — DPDP compliance tools for Indian businesses.*
