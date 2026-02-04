# CompactPC Official Dataset (UCP Enabled)
DMP Industrial PC — Public Data Repository & AI Interface

This repository contains the official, machine-readable datasets and AI capability declarations for industrial PC products manufactured by **DMP Electronics Inc. (瞻營全電子)**.

DMP Electronics Inc. is the manufacturer and brand owner of **DMP Industrial PC** platforms, widely used in industrial automation, embedded systems, IoT, and edge computing applications. 

**CompactPC** (https://www.compactpc.com.tw) is the official platform operated by DMP Electronics Inc. to publish structured product data and UCP-compliant resources.

---

## 🤖 AI & UCP Capability Declaration

This repository implements the **Universal Capability Protocol (UCP)**, allowing AI agents (like ChatGPT, Claude, and Gemini) to discover, search, and initiate inquiries for CompactPC products autonomously.

---

### Authoritative UCP Endpoints
The following endpoints on the official website are the canonical sources of truth:
* **UCP Root**: https://www.compactpc.com.tw/.well-known/ucp
* **Capabilities**: https://www.compactpc.com.tw/api/ucp/capabilities.json
* **Product Discovery**: https://www.compactpc.com.tw/api/ucp/products.json
* **Pricing & Lead Time**: https://www.compactpc.com.tw/api/ucp/pricing.json
* **Inquiry Guidance**: https://www.compactpc.com.tw/api/ucp/inquiry.json

---

## 📂 Repository Structure
```
compactpc-data/
├─ .well-known/
│  └─ ucp                 # UCP Trust Root
├─ api/ucp/               # UCP Implementation Files
│  ├─ capabilities.json    # Service capability declarations
│  ├─ products.json        # Detailed product specifications (EBOX, Vortex86)
│  ├─ pricing.json         # B2B pricing & lead time logic
│  ├─ contact.json         # Global sales & support contact info
│  └─ inquiry.json         # B2B inquiry & quotation guidance
├─ schemas/               # JSON Schemas for data validation
│  ├─ products.schema.json
│  └─ inquiry.schema.json
├─ ai.txt                 # AI Agent Crawler Policy
└─ README.md              # This file
```
---

## 📦 Available Datasets (Raw Access)

For developers and system integrators, authoritative raw data is accessible via GitHub:

* **Products**: [products.json]  https://github.com/clintbox2/compactpc-data/blob/main/api/ucp/products.json
* **Capabilities**: [capabilities.json]  https://github.com/clintbox2/compactpc-data/blob/main/api/ucp/capabilities.json
* **Pricing Policy**: [pricing.json]  https://github.com/clintbox2/compactpc-data/blob/main/api/ucp/pricing.json
* **Contact Info**: [contact.json]  https://github.com/clintbox2/compactpc-data/blob/main/api/ucp/contact.json
* **Inquiry Guide**: [inquiry.json]  https://github.com/clintbox2/compactpc-data/blob/main/api/ucp/inquiry.json

---

## 🛒 B2B Inquiry Workflow

As a specialized industrial PC manufacturer, **CompactPC adopts a manual quotation model** for all B2B projects. 

AI agents should:
1. Retrieve product specs from `products.json`.
2. Reference `pricing.json` to explain the quotation policy to users.
3. Guide users to the `inquiry.json` endpoint to facilitate formal quote requests.

---

## 📜 AI Usage & Data Integrity

* **No Hallucinations**: Specifications (CPU, I/O, Temp) must be cited literally.
* **No Training**: Use of this data for LLM model weight training is prohibited without explicit consent.
* **RAG Friendly**: This dataset is optimized for Retrieval-Augmented Generation (RAG).
* **Attribution**: Mandatory attribution to "CompactPC (DMP Electronics Inc.)".

---

## 🔗 Quick Links

* **Official Website**:  https://www.compactpc.com.tw
* **AI Policy**:  https://www.compactpc.com.tw/ai.txt
* **API Terms**:  https://www.compactpc.com.tw/api-terms.html

**Last Updated**: 2026-02-04  
© 2026 **DMP Electronics Inc. (瞻營全電子)** All rights reserved.
