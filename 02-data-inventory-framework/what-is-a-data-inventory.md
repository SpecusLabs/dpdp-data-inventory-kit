# What Is a Data Inventory?

**By Specus Labs**

---

> **Disclaimer:** This document is for informational purposes only. It does not constitute legal advice. Consult a qualified legal professional for advice specific to your organisation.

---

## The simple explanation

A data inventory is a documented record of all the personal data your organisation holds — what it is, where it lives, why you have it, who can access it, and how long you keep it.

Think of it as a map of your data estate.

Without this map, you are flying blind. You cannot build consent notices you do not understand. You cannot respond to erasure requests for data you cannot locate. You cannot secure data you did not know existed.

---

## What a data inventory is not

It is not a technical database schema.
It is not a privacy policy.
It is not a one-time audit report.
It is not something only lawyers or compliance professionals can build.

It is a living business document. It should be understandable by your operations lead, your developer, and your founder — and updated by all three.

---

## What a data inventory captures

A complete data inventory answers seven questions for every type of personal data you hold:

**1. What data?**
The category of personal data. For example: mobile number, delivery address, purchase history, employee PAN number.

**2. Where does it live?**
The system or location where this data is stored. For example: Shopify, a MySQL database, an Excel sheet, a WhatsApp group.

**3. Why do you have it?**
The purpose of processing. For example: to process and deliver orders, to send marketing emails, to process payroll.

**4. Who collected it?**
Was it collected directly from the individual, or received from another source (a partner, a vendor, a public database)?

**5. Who has access?**
Which teams, roles, or individuals can view or use this data? Which vendors or third-party systems can access it?

**6. Is it shared with anyone?**
Vendors, partners, government bodies, or other third parties who receive this data.

**7. How long do you keep it?**
The retention period — how long you store this data before deleting it.

---

## Why the DPDP Act requires you to know this

The DPDP Act (2023) places the following obligations directly on your organisation as a Data Fiduciary:

- **Section 4** — You may only process personal data for a lawful purpose. Without knowing what data you process, you cannot verify each purpose is lawful.
- **Section 6** — Consent notices must describe what data is collected and why. Without an inventory, your notices will be inaccurate or incomplete.
- **Section 8(7)** — Data must be deleted when no longer necessary. Without an inventory, you do not know what to delete or when.
- **Section 11** — You must respond to Data Principal access requests. Without an inventory, you cannot locate all data about a person.
- **Section 12** — You must respond to erasure requests. Without an inventory, you will miss data in systems you forgot about.
- **Section 8(6)** — In a breach, you must notify affected individuals. Without an inventory, you cannot determine who was affected.

---

## The two templates in this kit

### Master Inventory (`data-inventory-master.csv` / `.html`)

The full-featured inventory template. Captures all fields required for comprehensive DPDP compliance:

- System name and type
- Data categories held
- Data subjects (customers, employees, candidates, etc.)
- Purpose of processing
- Legal basis (consent, legitimate use, etc.)
- Source of data (collected directly or received)
- Internal access (teams and roles)
- Vendor sharing (Data Processors)
- Cross-border transfer (yes/no and destination)
- Retention period
- Deletion mechanism
- Risk level (Low / Medium / High)
- Children's data flag
- Last reviewed date and reviewed by

**Recommended for:** Funded startups, businesses preparing for audits, Significant Data Fiduciaries, businesses with complex vendor networks.

### Lite Inventory (`data-inventory-lite.csv`)

A streamlined version for businesses building their first data inventory. Captures the six most critical fields:

- System name
- Data categories held
- Purpose of processing
- Who has access
- Shared with which vendors
- Retention period

**Recommended for:** Early-stage businesses, small teams, businesses doing a first-pass inventory before upgrading to the master template.

---

## How to maintain your inventory

**Assign an owner.**
One person should be responsible for keeping the inventory current. In a small business, this is typically the founder or operations lead. In a larger business, this is the Data Protection Officer or Compliance Manager.

**Update on any of these triggers:**
- You onboard a new SaaS tool or vendor
- You launch a new product feature that collects data
- You expand into a new market or user segment
- A vendor you use changes their sub-processors
- You receive a data erasure or access request that reveals a gap
- You conduct an annual review

**Review schedule:**
- Minimum: Once a year
- Recommended: Once a quarter for growing businesses
- Required for Significant Data Fiduciaries: As per Data Protection Board guidance

**Version control:**
Date-stamp your inventory file each time you update it. Keep previous versions. This creates an audit trail.

---

## Where the inventory feeds into other compliance activities

| Compliance activity | How the inventory helps |
|---|---|
| Consent notices | Ensures notices describe what data is actually collected |
| Privacy policy | Provides the factual base for your policy |
| Vendor DPAs | Identifies which vendors need a Data Processing Agreement |
| Breach response | Tells you what data was exposed and who to notify |
| Data Principal rights requests | Lets you locate, compile, and deliver data quickly |
| Security assessment | Highlights where sensitive data is held and who has access |
| Data deletion | Documents what to delete, from where, and when |

---

*Built by [Specus Labs](https://github.com/specuslabs) — DPDP compliance tools for Indian businesses.*
