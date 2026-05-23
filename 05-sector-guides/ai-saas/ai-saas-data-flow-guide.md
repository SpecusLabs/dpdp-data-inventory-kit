# AI SaaS — Data Flow Guide

**By Specus Labs**

---

> **Disclaimer:** This document is for informational purposes only. It does not constitute legal advice. Consult a qualified legal professional for advice specific to your organisation.

---

## Overview

AI SaaS businesses face a data compliance challenge that is categorically different from other sectors. When a user types a prompt into your product, that input may contain personal data — their own, or data about other people. That prompt is then sent to a third-party AI API (OpenAI, Google, Anthropic, AWS Bedrock, Cohere) that may be located in the United States or Europe. The output is generated, returned, and often logged.

Most AI SaaS founders have not mapped this flow. This guide does it for you.

---

## What makes AI SaaS data flows distinct

**User-generated content contains personal data**
Prompts entered by users frequently contain names, email addresses, financial details, health information, or other personal data — even when users are not intending to share sensitive information. Your product design must account for this.

**Third-party AI APIs are Data Processors**
When you call OpenAI, Google Gemini, Anthropic Claude, or AWS Bedrock, you are sharing your users' input data with a third-party service. These companies are acting as Data Processors. A Data Processing Agreement is required.

**Training data risk**
Some AI API providers use API inputs to improve their models unless you explicitly opt out. If a user's personal data is used in training, you have created a data sharing scenario that almost certainly was not disclosed in your consent notice.

**Action:** Verify whether your AI API provider uses API inputs for training. Opt out if this is the default. Disclose your API provider in your privacy policy.

**Inference logs create a personal data store**
If you log model inputs and outputs for debugging or product improvement, those logs are personal data stores. They need retention periods, access controls, and deletion mechanisms.

**Embedding vectors may encode personal data**
If you use Retrieval-Augmented Generation (RAG) or semantic search, you are likely storing embedding vectors. Embeddings are numerical representations of text. If the original text contained personal data, the embeddings may also be considered personal data — or at minimum, may allow reconstruction of personal data.

---

## Data entry points

### 1. User registration
**Data collected:** Name, email, company name, role, phone (optional).

**DPDP obligation:** Consent required (Section 6). Standard SaaS registration — straightforward to address.

### 2. User prompt input
**Data collected:** Whatever the user types into your AI interface. May include their own personal data or data about third parties (their customers, colleagues, patients, etc.).

**DPDP obligation:** You must disclose in your privacy policy that user inputs are processed by your platform and sent to a third-party AI API. If users are processing personal data of their own customers via your product, you may need a Business Associate Agreement or Data Processing Agreement with your users as well.

### 3. File or document upload
**Data collected:** If your product allows document uploads for AI processing — these documents may contain large volumes of personal data (client lists, HR records, financial statements).

**DPDP obligation:** Disclose that uploaded documents are sent to your AI API. Confirm with your API provider whether document content is stored or used for training.

### 4. Integration connections (API keys, OAuth)
**Data collected:** If your product connects to users' external systems (CRM, email, database), you may be ingesting personal data from those systems.

**DPDP obligation:** Your product's access to external systems must be disclosed. Users must consent to the scope of access. Limit API permissions to the minimum required.

### 5. Usage and analytics
**Data collected:** Feature usage, session length, feature adoption, error logs, user journey data.

**DPDP obligation:** Standard analytics consent. Ensure no personal data from user prompts leaks into analytics events.

---

## Data flows to third parties

### Third-party AI API providers

Every call to an AI API sends the user's input (and often conversation context) to that provider's servers. All major providers are US-based.

| Provider | Data Processing Location | Default Training Opt-In | DPA Available |
|---|---|---|---|
| OpenAI API | USA | No (API inputs not used for training by default) | Yes — OpenAI DPA |
| Google Vertex AI / Gemini API | USA / EU options | No (by default for API) | Yes — Google Cloud DPA |
| Anthropic Claude API | USA | No (API inputs not used by default) | Yes — Anthropic DPA |
| AWS Bedrock | USA / India region available | No | Yes — AWS DPA |
| Cohere | USA / Canada | Check current policy | Yes — Cohere DPA |

**Action required for all providers:**
1. Confirm your API account type (some free tiers may use inputs for training — verify)
2. Download and sign the DPA from the provider
3. Disclose the provider's name and country in your privacy policy

### Analytics platforms
If you use Mixpanel, Amplitude, PostHog, or similar, ensure that user prompt text or AI output text is not included in analytics events. Only track behavioural metadata (feature clicked, session length, error codes).

### Customer support tools
Support tickets may contain descriptions of AI outputs or prompt content. Ensure your support tool (Intercom, Freshdesk) has a DPA in place.

---

## Inference logs — a specific risk area

If your product logs model inputs and outputs (which most do, for debugging and product improvement), those logs are a personal data store that most AI SaaS businesses have not inventoried.

Consider:
- Who has access to inference logs? (typically engineering team)
- How long are logs retained? (often indefinitely — this must change)
- Are logs searchable by user?
- Can you delete a specific user's log entries on an erasure request?
- Are logs stored in the same region as your other data?

**Recommended practice:**
- Set a maximum retention period for inference logs (30–90 days for debugging; longer only if justified)
- Implement log filtering to redact obvious personal data (email addresses, phone numbers) before storage
- Ensure deletion pipeline covers logs when a user account is deleted

---

## Training data risk

If you have fine-tuned a model using your own dataset, or plan to do so, that training data must be audited for personal data.

- Does your training dataset include user-generated content?
- If yes, did users consent to their inputs being used for model training?
- Does the dataset include any data from third-party sources?
- Is the training data stored securely with access controls?

**Action:** If training data contains personal data, it must be disclosed in your consent notice and privacy policy. If users did not consent to this use, the training data must be reviewed and potentially rebuilt.

---

## Embedding vectors and RAG systems

If your product uses RAG (Retrieval-Augmented Generation) or any form of semantic search over user documents, you are storing embedding vectors.

The legal status of embeddings is not yet settled under the DPDP Act. However, as a precautionary principle:
- Treat user-generated embeddings as personal data
- Include them in your retention and deletion policies
- Ensure deletion of embeddings when a user account is deleted or on erasure request
- Do not share embeddings with third parties without disclosure

---

## DPDP Act checklist for AI SaaS businesses

- [ ] Privacy policy discloses all third-party AI APIs used and their country of operation
- [ ] DPA signed with every AI API provider used (OpenAI, Anthropic, Google, AWS, Cohere)
- [ ] Verified that API inputs are NOT used for training by your provider (or opted out)
- [ ] Inference logs have a documented retention period (recommended: 30–90 days)
- [ ] Inference logs access restricted to engineering team with access logs
- [ ] Deletion pipeline covers inference logs on account deletion
- [ ] Embedding vectors included in retention and deletion policies (for RAG systems)
- [ ] Training data audited for personal data if fine-tuning has been done
- [ ] User consent notice describes what happens to prompt inputs
- [ ] Cookie consent and analytics consent implemented
- [ ] Access request process: can you retrieve all data held about a user? (Section 11)
- [ ] Erasure request process: can you delete all data including logs and embeddings? (Section 12)
- [ ] Children's data: age gate in place if product may be used by individuals under 18 (Section 9)

---

*Built by [Specus Labs](https://github.com/specuslabs) — DPDP compliance tools for Indian businesses.*
