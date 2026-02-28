## Problem Definition

### Overview
Classifying and routing fintech support tickets or payment‑related messages using an LLM with a reproducible evaluation loop.

Sentenial likely receives large volumes of incoming support or payment‑related messages that must be routed quickly and consistently. These messages are short, messy, and varied, and humans currently triage them manually.

---

### Input Schema
- **text** — unstructured user-generated message  
  Example: “The payment keeps failing on your platform.”

---

### Output Schema
- **label** — one of:
  - Billing issue  
  - Failed payment  
  - Account access / KYC  
  - Refund request  
  - Technical issue  
  - General question  

- **priority** — High, Medium, Low  
- **needs_human** *(optional)* — Yes, No  

These categories reflect the most common operational buckets in fintech support workflows and map directly to routing queues or specialized teams.

---

### Problem Statement
The goal is to build a lightweight, reliable LLM‑powered classifier that categorizes incoming fintech support messages into predefined categories and assigns a priority level. This enables faster routing, reduces manual sorting, and improves consistency in handling high‑volume support traffic.

---

### Focus Areas
- data clarity  
- a baseline LLM classifier  
- a reproducible evaluation loop  
- a simple iteration  
- integration thinking  

---

### Boundaries
This project does not include building a backend service, training large models from scratch, or implementing a full RAG system.
