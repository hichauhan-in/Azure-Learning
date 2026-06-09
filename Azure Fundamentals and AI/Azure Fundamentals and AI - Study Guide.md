# Azure Fundamentals and AI — Study Guide

> **Mode:** Pure learning (concepts from zero — no interview question bank or behavioral sections).
> **Goal:** Build a solid mental model of how Microsoft Azure works *and* how AI is built and consumed on Azure, starting from absolutely no prior knowledge.
> **Covers:** The ground commonly mapped to **AZ-900 (Azure Fundamentals)** and **AI-900 (Azure AI Fundamentals)**, explained plainly with diagrams and analogies.

---

## How this guide works
- Every term is explained **before** it's used, in plain English, with a real-world **analogy**.
- Diagrams (Mermaid) are used generously to show flows and comparisons.
- Each Part ends with a **✅ Quick Self-Check** (questions with answers to test yourself) and **🧠 30-Second Memory Hooks**.
- We build **one Part at a time**. Say **"next"** (or name a Part) and I'll write it. Say things like *"go deeper on X"*, *"make it simpler"*, or *"add more diagrams"* and I'll adapt and carry the style forward.

---

## The Learning Path (foundations → core → governance → AI → edge)

### 🟦 Group 1 — Cloud & Azure Foundations
| Part | Title | What you'll learn | Status |
|------|-------|-------------------|--------|
| A | [Cloud Computing Basics](prep/Part-A-cloud-basics.md) | What "the cloud" really is; IaaS/PaaS/SaaS; public/private/hybrid; CapEx vs OpEx; why organisations move to cloud | ✅ Done |
| B | [Azure Global Architecture](prep/Part-B-azure-architecture.md) | Regions, availability zones, datacenters; subscriptions, management groups, resource groups; Azure Resource Manager | ✅ Done |

### 🟩 Group 2 — Core Azure Services
| Part | Title | What you'll learn | Status |
|------|-------|-------------------|--------|
| C | [Compute Services](prep/Part-C-compute.md) | Virtual Machines & Scale Sets, App Service, Containers (ACI) & AKS, Azure Functions (serverless), Logic Apps, Event Grid/Hubs & Service Bus, Azure Virtual Desktop, Azure Arc — and when to use each | ✅ Done |
| D | [Networking](prep/Part-D-networking.md) | Virtual Networks & subnets, VPN Gateway, ExpressRoute, Load Balancer, Application Gateway, DNS, peering, CDN | ✅ Done |
| E | [Storage](prep/Part-E-storage.md) | Blob/File/Queue/Table storage, managed disks, access tiers, redundancy (LRS/ZRS/GRS), migration tools (AzCopy, Storage Explorer, Data Box), Backup & Site Recovery | ✅ Done |
| F | [Databases & Big Data](prep/Part-F-databases.md) | Azure SQL, Cosmos DB, managed MySQL/PostgreSQL; relational vs non-relational; analytics: Synapse, Databricks, HDInsight, Data Factory; IoT Hub & IoT Central | ✅ Done |
| G | [Identity (Microsoft Entra ID)](prep/Part-G-identity.md) | Authentication vs authorization, MFA, RBAC, conditional access, single sign-on, External ID | ✅ Done |

### 🟨 Group 3 — Management, Security & Governance
| Part | Title | What you'll learn | Status |
|------|-------|-------------------|--------|
| H | [Management & Monitoring Tools](prep/Part-H-management-tools.md) | Portal, CLI, PowerShell, Cloud Shell, ARM/Bicep templates, Azure Mobile App, Azure Monitor, Log Analytics, Application Insights, Service Health, Azure Advisor | ✅ Done |
| I | [Security](prep/Part-I-security.md) | Defense in depth, Zero Trust, Microsoft Defender for Cloud, Sentinel, Key Vault, NSGs, Azure Firewall, DDoS Protection, Bastion | ✅ Done |
| J | [Governance, Cost & SLAs](prep/Part-J-governance-cost.md) | Azure Policy, Blueprints, resource locks, tags, Cost Management, Pricing/TCO calculators, SLAs, service lifecycle, Trust Center & compliance | ✅ Done |

### 🟪 Group 4 — Artificial Intelligence on Azure
| Part | Title | What you'll learn | Status |
|------|-------|-------------------|--------|
| K | [AI & Machine Learning Fundamentals](prep/Part-K-ai-ml-fundamentals.md) | What AI/ML actually are; supervised/unsupervised/deep learning; Responsible AI principles | ✅ Done |
| L | [Azure AI Services Overview](prep/Part-L-azure-ai-services.md) | The Azure AI Services umbrella, keys & endpoints, multi-service vs single-service resources, how you consume prebuilt AI | ✅ Done |
| M | [Computer Vision](prep/Part-M-computer-vision.md) | Image analysis, OCR & Document Intelligence (Form Recognizer), face detection, Custom Vision | ✅ Done |
| N | [Natural Language, Speech & Search](prep/Part-N-language-speech.md) | Language service, sentiment, key phrases, entities, translation, speech-to-text & text-to-speech, conversational AI / Bot Service, Azure AI Search (knowledge mining) | ✅ Done |
| O | [Generative AI & Azure OpenAI](prep/Part-O-generative-ai.md) | LLMs, tokens, prompts, Azure OpenAI Service, Copilot, grounding/RAG basics, Responsible generative AI | ✅ Done |
| P | [Azure Machine Learning Service](prep/Part-P-azure-ml.md) | Workspaces, Designer, Automated ML, MLOps lifecycle | ✅ Done |

### 🟧 Group 5 — Tying It Together
| Part | Title | What you'll learn | Status |
|------|-------|-------------------|--------|
| Q | [Miscellaneous, Deeper Topics & Trends](prep/Part-Q-misc-trends.md) | Well-Architected & Cloud Adoption Frameworks, current trends, certification study tips (AZ-900 & AI-900) | ✅ Done |

---

**Status legend:** ⬜ Not started · 🟨 In progress · ✅ Done

➡️ **All Parts complete! ✅** Work through each Part in order, do the **✅ Quick Self-Checks** aloud, and review the **🧠 Memory Hooks** before exams. Then take an official practice assessment on Microsoft Learn for AZ-900 and AI-900.
