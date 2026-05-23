# DPDP Act — Key Sections for Data Inventory

**By Specus Labs**

---

> **Disclaimer:** This document is for informational purposes only. It does not constitute legal advice. Refer to the official text of the Digital Personal Data Protection Act, 2023 and consult a qualified legal professional for advice specific to your organisation.

---

## Why data inventory is a legal necessity, not just good practice

The DPDP Act does not mandate a "data inventory" by name. However, the obligations it places on Data Fiduciaries — your organisation — cannot be met without one. The sections below explain each obligation and how your data inventory directly enables compliance.

---

## Section 2 — Definitions

### Section 2(i) — Data Fiduciary
> An entity that determines the purpose and means of processing personal data.

**What this means for your inventory:**
Your organisation is the Data Fiduciary. You are responsible for all personal data processing within your systems — including data processed by vendors on your behalf. Your inventory must cover everything you control, even if a vendor does the actual processing.

### Section 2(j) — Data Processor
> An entity that processes personal data on behalf of a Data Fiduciary.

**What this means for your inventory:**
Every vendor that touches your personal data is a Data Processor. They must appear in your vendor data map. See `03-data-mapping-templates/vendor-data-map.csv`.

### Section 2(n) — Personal Data
> Data about an individual who is identifiable by or in relation to such data.

**What this means for your inventory:**
Your inventory must capture all data that can identify a person — directly or indirectly. This includes names, phone numbers, email addresses, device IDs, IP addresses, location data, purchase history, health data, and behavioural data. See `01-dpdp-reference/personal-data-categories-under-dpdp.md` for a full list.

### Section 2(x) — Processing
> Any operation performed on personal data — collection, recording, organisation, structuring, storage, adaptation, retrieval, use, disclosure, sharing, transmission, erasure, or destruction.

**What this means for your inventory:**
Processing covers far more than just "using" data. Storing it, backing it up, sharing it with a vendor, and deleting it are all processing activities. Your inventory should capture the full lifecycle.

---

## Section 4 — Grounds for processing personal data

**The obligation:** Personal data may only be processed for a lawful purpose — either with the consent of the Data Principal, or for certain legitimate uses specified in the Act.

**What this means for your inventory:**
Every row in your data inventory must have a documented **purpose**. If you cannot state why you hold a piece of data, you likely should not hold it.

Your inventory should capture:
- The purpose of processing for each data category
- Whether consent is the legal basis, or another ground under Section 4

---

## Section 6 — Consent

**The obligation:** Consent must be free, specific, informed, unconditional, and unambiguous. The consent notice must state what data is collected and the purpose of processing.

**What this means for your inventory:**
Your consent notices must match your inventory. If your inventory shows that you collect location data and share it with a logistics vendor, your consent notice must say so. Use the DPDP Consent Notice Kit alongside this toolkit.

---

## Section 8 — General obligations of Data Fiduciaries

### Section 8(1) — Purpose limitation
> Personal data may only be processed for the purpose for which consent was given.

**Inventory column:** Purpose of Processing

### Section 8(4) — Security safeguards
> Reasonable security safeguards must be implemented to prevent personal data breach.

**Inventory column:** Security Measures / Access Controls

### Section 8(6) — Breach notification
> In the event of a personal data breach, the Data Protection Board and affected Data Principals must be notified.

**What this means for your inventory:**
You cannot notify affected individuals if you do not know what data was held about them, where it was stored, and who had access. A completed inventory is essential for breach response.

### Section 8(7) — Data retention and erasure
> Personal data shall not be retained beyond the period necessary for the specified purpose.

**Inventory column:** Retention Period / Deletion Schedule

---

## Section 9 — Processing of personal data of children

**The obligation:** Verifiable parental consent is required before processing personal data of a child (individual under 18 years). Behavioural tracking of children is prohibited.

**What this means for your inventory:**
If any of your systems collect data from individuals who may be under 18, this must be flagged. Add a "Children's Data" column or flag in your inventory.

---

## Section 11 — Right of Data Principal to access information

**The obligation:** Data Principals have the right to request a summary of personal data held about them and the processing activities.

**What this means for your inventory:**
You cannot respond to an access request if you do not know where data is held. Your inventory enables you to locate, compile, and provide this summary. It also helps you understand which systems to query.

---

## Section 12 — Right to correction and erasure

**The obligation:** Data Principals have the right to request correction of inaccurate data and erasure of data that is no longer necessary.

**What this means for your inventory:**
To action an erasure request, you must know every system where a person's data exists. If your inventory is incomplete, you risk missing a system and failing to erase data as required.

---

## Section 13 — Right to grievance redressal

**The obligation:** Data Principals have the right to a grievance redressal mechanism.

**What this means for your inventory:**
Grievance handling often involves investigating what data was held and how it was processed. Your inventory provides the documentation to support this investigation.

---

## Section 16 — Significant Data Fiduciary obligations

**The obligation:** Businesses designated as Significant Data Fiduciaries (SDFs) must appoint a Data Protection Officer, conduct data protection impact assessments, and undertake periodic data audits.

**What this means for your inventory:**
If you are or may become an SDF, a detailed and regularly reviewed data inventory is a prerequisite for audits and DPIAs. Even if you are not yet an SDF, maintaining audit-ready documentation is good practice.

---

## Summary: Inventory columns mapped to DPDP obligations

| DPDP Obligation | Relevant Section | Inventory Column |
|---|---|---|
| Identify all personal data held | Section 2(n) | Data Categories |
| Document purpose of processing | Section 4, 8(1) | Purpose of Processing |
| Record legal basis | Section 4, 6 | Legal Basis / Consent Required |
| Identify all systems | Section 8(4) | System Name |
| Identify all vendors | Section 2(j) | Vendor / Data Processor |
| Security safeguards | Section 8(4) | Security Measures |
| Retention periods | Section 8(7) | Retention Period |
| Children's data flag | Section 9 | Children's Data (Y/N) |
| Cross-border transfers | Draft DPDP Rules | Transfer Outside India (Y/N) |

---

*Built by [Specus Labs](https://github.com/specuslabs) — DPDP compliance tools for Indian businesses.*
