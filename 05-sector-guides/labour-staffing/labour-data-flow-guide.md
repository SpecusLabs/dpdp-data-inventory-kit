# Labour Supply and Staffing — Data Flow Guide

**By Specus Labs**

---

> **Disclaimer:** This document is for informational purposes only. It does not constitute legal advice. Consult a qualified legal professional for advice specific to your organisation.

---

## Overview

Labour supply and staffing businesses hold some of the most sensitive personal data of any sector. Candidate data — resumes, government IDs, bank details, background verification reports — flows across multiple parties: your internal team, client businesses, background verification agencies, payroll processors, and often informal channels like WhatsApp.

This guide walks through how data typically flows in a labour staffing or workforce supply business, what the DPDP Act requires at each stage, and what actions to take.

---

## The data problem in staffing businesses

The pain point is universal: "I don't know where and how the data flows."

In a typical staffing business, a single candidate's data will touch:
- Your WhatsApp group (initial outreach and document collection)
- Your recruiter's personal email (resume received)
- A shared Google Sheet (tracker for placements)
- A Google Drive folder (ID documents uploaded)
- A background verification agency (data shared for BGV)
- Your client's HR system (candidate details sent for placement)
- Your payroll processor (bank details sent for salary disbursement)
- Government portals (PF/ESI registration)

This data flow is largely undocumented and often unprotected. The DPDP Act requires you to document and control it.

---

## Data entry points

### 1. Job application (portal, referral, or WhatsApp)
**Data collected:** Name, phone, email, current location, work experience summary, desired role.

**DPDP obligation:** Consent required at the point of application (Section 6). WhatsApp-based intake has no consent mechanism — this must be addressed.

**Action:** Create a digital intake form (Google Form, Typeform, or your own portal) with a consent checkbox that describes what data you collect and why. Stop collecting applications via personal WhatsApp as a primary channel.

### 2. Document collection during onboarding
**Data collected:** Aadhaar card, PAN card, bank account details, address proof, educational certificates, photograph.

**DPDP obligation:** This is highly sensitive data. Consent must be specific — the candidate must know exactly why each document is needed and who it will be shared with. Aadhaar collection is subject to UIDAI guidelines in addition to DPDP.

**Action:** Issue a written data collection notice at the time of document submission. State each document, the reason it is collected, and who it will be shared with.

### 3. Interview and assessment
**Data collected:** Interview notes, assessment scores, interviewer observations, video recordings (if interviews are recorded).

**DPDP obligation:** Inform candidates if interviews are recorded. Recruitment decisions based on data must be supported by a documented process.

### 4. Background verification
**Data collected:** Criminal record check, employment history verification, educational credential check, address verification. Often involves sharing Aadhaar or PAN with the BGV agency.

**DPDP obligation:** Specific consent required for BGV. The BGV agency is a Data Processor — a DPA is required. Candidates must be informed that BGV will be conducted and what agencies will be used.

### 5. Client data submission
**Data collected:** You may receive personal data about client employees or client HR contacts as part of the engagement.

**DPDP obligation:** You are acting as a Data Processor for the client in this context. Ensure your agreement with the client includes data protection terms.

---

## Data storage locations — typical staffing business

| System / Location | Data Stored | Risk Level | Action Required |
|---|---|---|---|
| WhatsApp Business / personal WhatsApp | Candidate name, phone, documents received | High | Stop using personal WhatsApp for document exchange. Move to a formal intake process. |
| Google Drive / Dropbox | Scanned Aadhaar, PAN, photos, certificates | High | Restrict access by folder. Enable 2FA on Google account. Audit who has access. |
| Google Sheet (candidate tracker) | Name, phone, current status, placement details | High | Restrict sharing. Remove ex-staff access. Set access expiry where possible. |
| Recruiter personal email | Resumes and documents received informally | High | Stop using personal email for candidate documents. Use a company email domain. |
| Company email | Resumes, client requirements, candidate communications | Medium | Ensure company email accounts are secured with 2FA. Define retention period. |
| BGV agency portal | Aadhaar, PAN, employment history shared for verification | High | DPA required with BGV agency. Confirm data is deleted post-verification. |
| Client HR system (external) | Candidate details shared with client post-placement | Medium | Ensure client agreement covers data protection. |
| Payroll software or bank transfer sheet | Bank account, IFSC, salary details | High | Restrict access. Use payroll software rather than manual bank transfer sheets where possible. |
| Government portals (EPFO, ESIC) | PF and ESI registration data — name, Aadhaar, bank | Low (regulated) | Government-regulated. Retain as per statutory requirements. |

---

## DPDP Act obligations specific to staffing

### Candidate data that is not used

If a candidate applies and is not placed or hired, their data may no longer serve any purpose. Under Section 8(7) of the DPDP Act, it must be deleted.

**Recommended practice:** Set a 12-month window from last contact. If no placement and no active engagement, delete candidate data from all systems.

### Data shared with clients

When you share a candidate's resume and details with a client company, the candidate should know this will happen. Your intake consent notice should state that their data may be shared with potential employers.

### WhatsApp-based recruitment

WhatsApp is widely used in labour staffing for both candidate outreach and document collection. This creates several problems:
- No consent mechanism
- No retention control
- No deletion capability at scale
- Documents shared in WhatsApp are accessible to everyone in a group

**Action:** WhatsApp may continue to be used for initial outreach and communication, but documents should not be collected via WhatsApp. Use a digital form with file upload for document collection.

---

## Data deletion obligations

| Data Category | Suggested Retention | Reason |
|---|---|---|
| Candidate data — not placed | 12 months from last contact | No ongoing purpose |
| Candidate data — placed, employment ended | 3 years from placement end | Dispute resolution, reference requests |
| Employee payroll records | 8 years | Statutory requirement (Income Tax, PF) |
| Background verification reports | Duration of engagement + 2 years | Workplace safety and verification records |
| Government ID scans (Aadhaar, PAN) | Duration of engagement only | Delete after completing statutory registrations |
| Client contact data | Duration of client relationship + 2 years | Business records |

---

## DPDP Act checklist for staffing businesses

- [ ] Digital intake form with consent checkbox — replacing WhatsApp-only intake (Section 6)
- [ ] Document collection notice — lists each document, purpose, and who it is shared with
- [ ] Candidate database has restricted access — not open to all staff
- [ ] Google Drive folders with ID documents have access controls
- [ ] DPA in place with background verification agency
- [ ] DPA in place with payroll processor
- [ ] Client agreement includes data protection clause
- [ ] Deletion process for non-placed candidates (12-month trigger)
- [ ] HR data restricted to 2–3 named individuals only
- [ ] Personal WhatsApp not used for document exchange
- [ ] Government ID scans deleted after statutory registration is complete
- [ ] Candidate access request process documented (Section 11)
- [ ] Candidate erasure request process documented (Section 12)

---

*Built by [Specus Labs](https://github.com/specuslabs) — DPDP compliance tools for Indian businesses.*
