# Usage Guide — DPDP Data Inventory Kit

**By Specus Labs**

---

> **Disclaimer:** This guide is for informational purposes only. It does not constitute legal advice. Consult a qualified legal professional for advice specific to your organisation.

---

## Before you begin

A data inventory project can feel overwhelming if you try to do everything at once. This guide breaks it into five stages. Most businesses can complete a working first draft in two to three days of focused effort.

You will need:
- A spreadsheet tool (Excel, Google Sheets, or similar) to edit the CSV files
- A browser to view the HTML templates
- Input from at least one person who knows your tech stack (developer, IT lead, or operations manager)
- Input from at least one person who knows your vendor contracts (founder, legal, or procurement)

---

## Stage 1 — Understand what you are mapping

Read `02-data-inventory-framework/what-is-a-data-inventory.md` before touching any template.

Key concepts to understand:

**Personal data** — Under Section 2(t) of the DPDP Act, personal data means any data about an individual who is identifiable by or in relation to such data. This includes obvious items like names, phone numbers, and email addresses, and less obvious items like device IDs, IP addresses, and behavioural data.

**Data Fiduciary** — Your organisation. The entity that determines the purpose and means of processing personal data (Section 2(i)).

**Data Principal** — The individual whose data you hold. Your customer, employee, user, or candidate.

**Processing** — Anything done with personal data. Collection, storage, use, sharing, deletion. All of it (Section 2(x)).

---

## Stage 2 — List your systems

Before filling any template, write a rough list of every system your business uses that touches personal data.

Prompt questions:
- Where does customer data first enter your business? (Website form, app, WhatsApp, phone call?)
- Where is it stored? (CRM, spreadsheet, database, email inbox?)
- Where is it processed? (Analytics platform, email marketing tool, payment gateway?)
- Where is it shared? (Logistics partner, accountant, support tool, marketing agency?)
- Where does employee or contractor data live? (HR system, payroll software, WhatsApp groups?)

Write this list on paper or in a blank document first. Do not skip this step. It will make filling the templates significantly faster.

---

## Stage 3 — Choose your template

### Option A: Lite inventory (recommended for businesses under 50 employees or early-stage compliance)

File: `02-data-inventory-framework/data-inventory-lite.csv`

This version captures the most important columns only:
- System name
- Data categories held
- Purpose of processing
- Who has access
- Shared with which vendors
- Retention period

Complete this first. You can always upgrade to the master inventory later.

### Option B: Master inventory (recommended for funded businesses, SIGs, or those preparing for audits)

File: `02-data-inventory-framework/data-inventory-master.csv`

This version captures all fields including legal basis, cross-border transfer status, risk level, and review dates.

---

## Stage 4 — Fill sector-specific templates

Go to `05-sector-guides` and open the folder for your sector.

Each sector folder contains:
- A pre-filled CSV with the most common systems and data types for that sector
- An HTML version of the same inventory
- A narrative flow guide explaining how data typically moves in that sector

**D2C e-commerce** — `05-sector-guides/d2c-ecommerce/`
Covers Shopify, Razorpay, Shiprocket, Klaviyo, Meta Ads, and similar platforms.

**Labour and staffing** — `05-sector-guides/labour-staffing/`
Covers candidate onboarding, document collection, client data sharing, payroll, and WhatsApp-based communication flows.

**AI SaaS** — `05-sector-guides/ai-saas/`
Covers user-generated inputs to models, third-party API data sharing (OpenAI, Google, AWS), training data, and logging practices.

Instructions for filling sector templates:
1. Open the CSV in your spreadsheet tool
2. Delete rows that do not apply to your business
3. Add rows for systems not already listed
4. Fill in the blank columns for each row
5. Save a copy with your organisation name in the filename

---

## Stage 5 — Map your data flows

Open `04-data-flow-diagrams/data-flow-template.html` in a browser.

This interactive template lets you:
- Click to add systems as nodes
- Draw arrows to show data movement between systems
- Label arrows with the data type being transferred
- Print or export as a visual for internal documentation

Also complete the checklist at `04-data-flow-diagrams/data-flow-checklist.md`. This text-based checklist is useful for team discussions and documentation even if you do not use the visual template.

---

## What to do with your completed inventory

Once complete, your data inventory should be:

**Stored securely** — Treat the inventory itself as sensitive. It lists exactly what data you hold and where. Store it in a password-protected location with access limited to those who need it.

**Reviewed regularly** — Set a review date (quarterly is recommended for growing businesses; at minimum annually). Add a calendar reminder. The inventory is a living document, not a one-time exercise.

**Used to drive other compliance activities:**

| Inventory finding | Action |
|---|---|
| System holds personal data with no documented purpose | Document the purpose or stop collecting |
| Data shared with vendor but no DPA in place | Use the DPDP Vendor Compliance Kit to issue a DPA |
| Data retained beyond stated period | Set up deletion schedules |
| No consent record for marketing data | Use the DPDP Consent Notice Kit to establish consent flows |
| Cross-border data transfer identified | Assess against DPDP Rules requirements |

---

## Common mistakes to avoid

**Mapping only your main product database**
Most businesses find that personal data lives in far more places than expected — email inboxes, support tools, WhatsApp groups, shared spreadsheets. Cast the net wide.

**Listing systems but not data types**
"Our CRM" is not sufficient. What data does your CRM hold? Names, phone numbers, purchase history, communication logs? Be specific.

**Ignoring employee and contractor data**
The DPDP Act applies to all personal data. Employee records, payroll data, contractor agreements, and HR documentation are all in scope.

**Treating the inventory as a one-time task**
Every new system you onboard, every new vendor you engage, every new data collection point you add should trigger an update to your inventory.

**Not involving your tech team**
The people who build and manage your systems know where data actually lives. Compliance cannot do this exercise without them.

---

## Questions and support

For questions about this toolkit, open an issue at [github.com/specuslabs/dpdp-data-inventory-kit](https://github.com/specuslabs/dpdp-data-inventory-kit).

For platform access and tailored compliance support, visit [dpdp-platform-specuslabs.up.railway.app](https://dpdp-platform-specuslabs.up.railway.app).

---

*Built by [Specus Labs](https://github.com/specuslabs) — DPDP compliance tools for Indian businesses.*
