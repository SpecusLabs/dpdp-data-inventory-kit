# Data Mapping Overview

**By Specus Labs**

---

> **Disclaimer:** This document is for informational purposes only. It does not constitute legal advice. Consult a qualified legal professional for advice specific to your organisation.

---

## What data mapping is

Data mapping is the process of documenting relationships between data, systems, and the people who use or are affected by that data.

While your data inventory answers "what data do you hold?", your data maps answer:

- **System data map** — Which systems hold which data? What does each system do with it?
- **Vendor data map** — Which vendors receive personal data from you? Under what terms?
- **Data subject category map** — Whose data do you hold? What categories of people are in your data estate?

These three maps, together with your master inventory, give you a complete picture of your data estate.

---

## Why three separate maps?

Different compliance activities require different views of your data.

| Activity | Most useful map |
|---|---|
| Security assessment and access controls | System data map |
| Vendor DPA issuance and management | Vendor data map |
| Responding to Data Principal rights requests | Data subject category map |
| Breach response — identifying affected individuals | Data subject category map + System data map |
| Consent notice drafting | All three |

---

## Templates in this folder

### `system-data-map.csv` and `.html`
Documents every system in your estate: what data it holds, who has access, how data enters and exits, and what security measures are in place.

Use this to:
- Understand which systems are high-risk
- Identify systems without documented access controls
- Feed into your IT security review

**DPDP Act relevance:** Section 8(4) — Security safeguards

### `vendor-data-map.csv` and `.html`
Documents every third-party vendor or partner that receives personal data from your organisation.

Use this to:
- Identify which vendors need a Data Processing Agreement (DPA)
- Understand what data each vendor can access
- Track whether a DPA is in place and when it expires

**DPDP Act relevance:** Section 2(j) — Data Processor obligations; Section 8 — Data Fiduciary responsibilities for processors

### `data-subject-category-map.csv` and `.html`
Documents the categories of individuals (Data Principals) whose data you hold.

Use this to:
- Understand whose data you are responsible for
- Identify categories requiring special attention (children, employees, candidates)
- Map rights requests to the correct systems

**DPDP Act relevance:** Section 11 — Right to access; Section 12 — Right to correction and erasure; Section 9 — Children's data

---

## How to fill these maps

**Step 1** — Complete your data inventory first (see `02-data-inventory-framework`)

**Step 2** — Use the inventory rows to populate the system data map. One row per system.

**Step 3** — From your inventory, extract every vendor listed under "Vendor / Data Processor". These populate your vendor data map.

**Step 4** — From your inventory, extract every unique category of Data Principal. These populate your data subject category map.

The maps are derived from your inventory — they should not contradict it. If a vendor appears in a map but not the inventory, update the inventory first.

---

## Using the HTML versions

The HTML templates for each map are interactive:
- Click cells to edit
- Use the Export CSV button to save your completed map
- Use Print / PDF to create a static document for records

---

*Built by [Specus Labs](https://github.com/specuslabs) — DPDP compliance tools for Indian businesses.*
