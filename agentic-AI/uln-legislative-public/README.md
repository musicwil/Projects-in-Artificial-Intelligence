# ⚖️ Understanding the Laws of the Nation (ULN)
### *Demystifying Legalese for the Modern Citizen*

## **The Mission**
The ULN project is designed to bridge the gap between dense, specialized "Legalese" and the everyday language used by the public. Our goal is to provide a central, intuitive interface where citizens can consult published laws, judicial opinions, and executive actions to receive clear, non-partisan, and actionable insights.

This prototype demonstrates a production-ready pipeline that transforms raw government data into **Public Service Impact Statements**, ensuring that every citizen—regardless of legal background—can understand how new legislation and government directives affect their lives.

## **Core Features**
* **Plain-Language Interface:** A user-centric design focused on making complex legal topics searchable and digestible.
* **The Transparency Engine:** A multi-agentic system that automates the extraction, classification, and interpretation of federal legislation and **Executive Orders**.
* **Verified Integrity:** To ensure 100% factual accuracy and zero political bias, the system utilizes a **Judicial Bench (LLM-as-a-Judge)** architecture. This allows three independent models to audit every summary before it reaches the public.

## **Technical Workflow (Powered by Google ADK)**
This project is built using the **Google Generative AI Agent Development Kit (ADK)**, utilizing its modular orchestration to manage complex agent interactions:

1. **Extraction & Classification:** Identifying mandates, dollar amounts, and effective dates from raw text.
2. **Plain-Language Interpretation:** Translating technical jargon and "Legalese" into accessible, common language.
3. **Multi-Model Audit:** A verification layer where Gemini, GPT-4o, and Claude cross-examine the output to ensure neutral tone and factual anchoring.
4. **Final Consensus:** Issuing the official Public Service Impact Statement through a centralized ADK Runner.

## **The Road to Phase 2**
* **Real-Time Integration:** Connecting live to Congress.gov (Legislative), SCOTUS (Judicial), and the **Federal Register API** (Executive Orders).
* **Scalability:** Moving from a localized prototype to a global production environment using **Google Cloud SQL**.
* **Global Search:** Implementing a comprehensive UI for historical and real-time law consultation.
