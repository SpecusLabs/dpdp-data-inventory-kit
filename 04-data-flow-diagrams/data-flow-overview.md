# Data Flow Overview

**By Specus Labs**

---

> **Disclaimer:** This document is for informational purposes only. It does not constitute legal advice. Consult a qualified legal professional for advice specific to your organisation.

---

## What is a data flow diagram?

A data flow diagram (DFD) is a visual map of how personal data moves through your organisation — from the moment it enters (collection) to the moment it is deleted (erasure).

Where your data inventory tells you *what* you hold, a data flow diagram tells you *how it moves*.

---

## Why data flow matters under the DPDP Act

The DPDP Act governs personal data at every stage of its lifecycle — not just storage. Understanding data flow helps you:

- Identify every point where personal data enters your organisation (consent obligations arise here)
- Identify every point where data is shared with a third party (Data Processor obligations arise here)
- Identify every point where data crosses a border (DPDP Rules compliance required)
- Map the path data must travel to reach a deletion endpoint (erasure rights under Section 12)
- Identify gaps — data leaving your organisation through informal channels (email, WhatsApp) without documentation

---

## The five stages of a data flow

Every personal data flow has five stages. Use these as your mapping framework:

**1. Collection**
Where does personal data first enter your organisation?
Examples: website checkout form, job application portal, WhatsApp message, sales call, third-party data purchase.

**2. Storage**
Where is personal data stored after collection?
Examples: Shopify database, internal MySQL, HR spreadsheet, CRM, email inbox.

**3. Processing**
Where and how is personal data used?
Examples: Klaviyo uses it for email campaigns; an analytics platform aggregates it for reporting; a logistics system uses address data for delivery routing.

**4. Transfer**
Where does personal data go outside your organisation (or to a different system within it)?
Examples: shared with a logistics vendor, sent to a marketing agency, uploaded to a cloud advertising platform, emailed to an accountant.

**5. Deletion**
Where and how is personal data deleted when no longer needed?
Examples: automated deletion on account closure, manual deletion on a schedule, purge from marketing list on unsubscribe.

---

## Templates in this folder

### `data-flow-template.html`
An interactive, browser-based data flow diagram builder. Allows you to:
- Add system nodes visually (entry points, storage, processors, third parties, deletion)
- Connect nodes with arrows labelled with data type
- Annotate each connection with DPDP Act references
- Print or export as a visual record

**How to use:**
1. Open in any modern browser
2. Click "Add Node" to add a system or actor
3. Select a node type (Entry Point, Storage, Processor, Third Party, Deletion)
4. Draw connections between nodes
5. Label each connection with the data being transferred
6. Use the Export button to save as an image or print to PDF

### `data-flow-checklist.md`
A text-based checklist for mapping data flows without the visual tool. Useful for:
- Team discussions and workshops
- Documentation in a text-based system
- Audit preparation

---

## Tips for mapping data flows

**Map one data subject category at a time**
Start with your largest group — typically customers. Trace every piece of customer data from collection to deletion. Then repeat for employees, candidates, and so on.

**Follow the data, not the org chart**
Data flows do not follow your reporting structure. A customer's phone number might travel from your Shopify checkout to a logistics vendor to a last-mile carrier to a delivery agent's device. Map the full chain.

**Do not forget informal channels**
Personal data often flows through channels that are not considered systems: email attachments, WhatsApp groups, printed documents. These must be in your flow map even if they are hard to control.

**Update your flow map when you change systems**
Every new tool or integration is a new data flow. Revisit the map whenever you onboard a new vendor or launch a new feature.

---

*Built by [Specus Labs](https://github.com/specuslabs) — DPDP compliance tools for Indian businesses.*
