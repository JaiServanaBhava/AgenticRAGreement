<div align="center">

<a name="top"></a>

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=220&section=header&text=📜%20AgenticRAGreement&fontSize=60&fontAlignY=40&desc=An%20Agentic%20RAG%20System%20with%20Human-in-the-Loop%20Agreement%20Governance&descAlignY=60&descSize=18&animation=twinkling" width="100%"/>

<br/>
<p align="center">
<a href="#-overview"><img src="https://img.shields.io/badge/🔗%20Overview-FF6B9D?style=for-the-badge&logoColor=white" alt="Overview"/></a>&nbsp;
<a href="#-demo"><img src="https://img.shields.io/badge/▶️%20Demo-00C853?style=for-the-badge&logoColor=white" alt="Demo"/></a>&nbsp;
<a href="#%EF%B8%8F-architecture"><img src="https://img.shields.io/badge/🧠%20Architecture-2979FF?style=for-the-badge&logoColor=white" alt="Architecture"/></a>&nbsp;
<a href="#-risk-grading"><img src="https://img.shields.io/badge/⚠️%20Risk%20Grading-FF9100?style=for-the-badge&logoColor=white" alt="Risk Grading"/></a>&nbsp;
<a href="#-colab-quickstart"><img src="https://img.shields.io/badge/☁️%20Colab-FF6D00?style=for-the-badge&logo=googlecolab&logoColor=white" alt="Colab"/></a>&nbsp;
<a href="#-roadmap"><img src="https://img.shields.io/badge/🗺️%20Roadmap-8E24AA?style=for-the-badge&logoColor=white" alt="Roadmap"/></a>
</p>

<p align="center">
<img src="https://img.shields.io/badge/Python-3.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
<img src="https://img.shields.io/badge/Gradio-5.0%2B-FF4B4B?style=for-the-badge&logo=gradio&logoColor=white" alt="Gradio"/>
<img src="https://img.shields.io/badge/Gemini_AI-2.5_Flash-8E75B2?style=for-the-badge&logo=googlegemini&logoColor=white" alt="Gemini"/>
<img src="https://img.shields.io/badge/Sentence_Transformers-all--MiniLM--L6--v2-FFCC00?style=for-the-badge&logo=huggingface&logoColor=black" alt="Embeddings"/>
<img src="https://img.shields.io/badge/License-MIT-00C853?style=for-the-badge&logo=opensourceinitiative&logoColor=white" alt="License"/>
</p>

<p align="center">
<img src="https://img.shields.io/badge/UI-3D%20Rainbow%20Glass-ff0055?style=for-the-badge&logo=css3&logoColor=white" alt="UI Theme"/>
<img src="https://img.shields.io/badge/HITL-✋%20Human--Approved-2979FF?style=for-the-badge" alt="HITL"/>
<img src="https://img.shields.io/badge/Privacy-🔒%20Local%20First-F75C7E?style=for-the-badge" alt="Privacy"/>
</p>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" width="100%"/>
<div align="center">

### 🟢 `✅ Answers from your verified notes first`
### 🟣 `🤖 Intelligent Gemini AI fallback second`
### 🟠 `✋ Complete human approval control — always`

</div>
</div>

<br/>

## 📌 Table of Contents

- [🌟 Overview](#-overview)
- [🧠 System Architecture & Workflow](#️-system-architecture--workflow)
- [🛡️ Risk Grading Engine](#-risk-grading-engine)
- [💡 Key Advantages](#-key-advantages)
- [⚡ Problem Solving Matrix](#-problem-solving--risk-mitigation)
- [💻 Running in Google Colab](#-running-in-google-colab)
- [🧰 Tech Stack](#-tech-stack)
- [🗺️ Roadmap](#-roadmap)
- [📜 License](#-license)

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" width="100%"/>

## 🌟 Overview

<div align="center">
<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=20&pause=1200&color=00C853&center=true&vCenter=true&width=850&lines=Next-generation+agentic+RAG+for+contract+analysis;Semantic+search+over+your+verified+knowledge+vault;Human-in-the-loop+governance+on+every+write" alt="Overview Typing"/>
</div>

**AgenticRAGreement** is a next-generation, agentic **Retrieval-Augmented Generation (RAG)** assistant designed for rigorous **contract, agreement, and policy document** analysis. 🧾

Unlike traditional black-box chatbots 🚫, AgenticRAGreement guarantees **full transparency and security** by checking your local verified knowledge base first using **semantic vector search**. If a query falls outside your verified documents, **Gemini AI** proposes a candidate answer — which is **only** written to your markdown vault and indexed upon your **explicit approval**. ✋

> 🎯 **The golden rule:** *Nothing enters your vault without you saying so.*

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" width="100%"/>

## 🧠 System Architecture & Workflow

```mermaid
graph TD
    A[👤 User Query Input] --> B[🔢 Sentence-Transformers Embedding]
    B --> C{📏 Semantic Similarity ≥ 0.30?}
    C -- ✅ Yes --> D[📘 Retrieve Verified Local Note]
    C -- ❌ No --> E[🤖 Query Gemini AI Fallback]
    E --> F[✋ Present Approval Dialog to User]
    F -- 👍 Approved --> G[📝 Append to Markdown Vault & Re-index Instantly]
    F -- 👎 Rejected --> H[🗑️ Discard Candidate Draft]
    D --> I[🖥️ Render Response in Chat UI]
    G --> I
    style A fill:#2979FF,stroke:#fff,color:#fff
    style D fill:#00C853,stroke:#fff,color:#fff
    style G fill:#FF9100,stroke:#fff,color:#fff
    style H fill:#D50000,stroke:#fff,color:#fff
```

<details>
<summary><b>🔍 Click to expand: How the agentic pipeline works</b></summary>

1. **📝 Ingest** — Documents are chunked and embedded with `all-MiniLM-L6-v2`.
2. **🎯 Retrieve** — Cosine similarity search returns the best local match.
3. **🤖 Fallback** — Low similarity triggers a Gemini 2.5 Flash draft.
4. **✋ Approve** — You review the draft in a dialog. Approve or reject.
5. **💾 Commit** — Approved drafts are appended to the vault and re-indexed live.
6. **📊 Grade** — Every response carries a live risk badge 🔴🟡🟢.

</details>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" width="100%"/>

## 🛡️ Risk Grading Engine

AgenticRAGreement goes beyond simple text retrieval by **automatically auditing** agreements and policies for predatory clauses and hidden risks. Every response is dynamically graded to protect your interests:

<div align="center">

| Grade | Meaning | Detected Issues |
| :---: | :--- | :--- |
| 🔴 **Critical Danger** | Severe legal traps detected | Total liability waivers, forced arbitration, data selling loops, silent background data harvesting |
| 🟡 **Caution** | Ambiguous or restrictive terms | Catch-all phrases, auto-renewal traps, unilateral modification rights |
| 🟢 **Safe / Low Risk** | Standard & fair provisions | Operational clauses, transparent user guidelines |

</div>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" width="100%"/>

## 💡 Key Advantages

<div align="center">
<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=18&pause=1000&color=2979FF&center=true&vCenter=true&width=800&lines=🚫+No+hallucinated+legal+text;👑+You+control+every+write;⚡+Instant+local+retrieval;🔒+Privacy-first+by+design" alt="Advantages"/>
</div>

- 🕳️ **Zero-Blind-Spots Audit:** Unlike generic LLMs that hallucinate legal text, AgenticRAGreement cross-references every phrase against your curated compliance vault.
- 👑 **Complete User Sovereignty:** No automated background writes or unverified data ingestion. You hold the master switch over what gets committed.
- ⚡ **Blazing Fast Local Retrieval:** Semantic vector search processes queries instantly using lightweight local embeddings (`all-MiniLM-L6-v2`).
- 🔒 **Privacy-First Design:** Sensitive corporate agreements and terms remain local and secure under your direct management.

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" width="100%"/>

## ⚡ Problem Solving & Risk Mitigation

| 😤 Challenge in Traditional T&Cs | 🦾 How AgenticRAGreement Solves It |
| :--- | :--- |
| **🕳️ Buried Legal Traps** | Instantly scans fine print to surface hidden liability waivers and class-action bans. |
| **🔄 Unilateral Changes** | Tracks modifications and flags clauses allowing companies to alter terms retroactively. |
| **👁️ Aggressive Data Tracking** | Exposes background device harvesting, device fingerprinting, and third-party data sales. |

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" width="100%"/>

## 💻 Running in Google Colab

You can test and run **AgenticRAGreement** instantly inside a Google Colab notebook with **zero local environment setup**. ☁️

1. 🌐 **Open Google Colab**: Head over to [Google Colab](https://colab.research.google.com/) and start a **New Notebook**.
2. 🔑 **Configure Your API Key**:

- Click on the **🔑 Key icon (Secrets)** on the left sidebar of Colab.
- Add a new secret with the name `GEMINI_API_KEY` and paste your Google Gemini API key.

3. 📦 **Install Core Dependencies**: Paste and run this command in your first code cell:

```python
   %pip install -q sentence-transformers google-generativeai gradio
```

4. 🧠 **Initialize Knowledge Base & Agent Core**: Set up your local markdown vault folders (`knowledge/fraud/`, `knowledge/agreements/`), load your embedding model (`all-MiniLM-L6-v2`), and configure the Gemini API client using Colab secrets:

```python
   import google.generativeai as genai
   from google.colab import userdata

   genai.configure(api_key=userdata.get("GEMINI_API_KEY"))
   gemini = genai.GenerativeModel("gemini-2.5-flash")
```

5. 🚀 **Launch the Gradio App**: Execute your Gradio blocks cell to spin up the interactive user interface:

```python
   demo.launch(share=True, debug=False)
```

6. 🎮 **Interact & Audit**: Click the public `gradio.live` URL generated in the output console to test terms and conditions safety risks, view real-time risk grading, and approve new knowledge entries right from your browser! 🚀

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" width="100%"/>

## 🧰 Tech Stack

<div align="center">

| Layer | Technology | Badge |
| :--- | :--- | :--- |
| 🧠 AI Model | Google Gemini 2.5 Flash | <img src="https://img.shields.io/badge/Gemini-2.5_Flash-8E75B2?style=flat-square&logo=googlegemini&logoColor=white"/> |
| 🔢 Embeddings | `all-MiniLM-L6-v2` | <img src="https://img.shields.io/badge/HuggingFace-MiniLM-FFCC00?style=flat-square&logo=huggingface&logoColor=black"/> |
| 🖥️ UI | Gradio 5.0+ | <img src="https://img.shields.io/badge/Gradio-5.0+-FF4B4B?style=flat-square&logo=gradio&logoColor=white"/> |
| 💾 Storage | Local Markdown Vault | <img src="https://img.shields.io/badge/Vault-Markdown-00C853?style=flat-square&logo=markdown&logoColor=white"/> |
| 🔎 Retrieval | Cosine Similarity ≥ 0.30 | <img src="https://img.shields.io/badge/Vector_Search-FAISS-2979FF?style=flat-square"/> |

</div>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" width="100%"/>

## 🗺️ Roadmap

We are continuously evolving AgenticRAGreement to make legal document and terms analysis smarter and more robust:

- [ ] 🌐 **Live URL Scraper:** Direct input of public Terms of Service or Privacy Policy web links for instant automated parsing.
- [ ] 📊 **Batch Document Analytics:** Multi-file drag-and-drop comparison matrix to contrast terms across competing services.
- [ ] ⚙️ **Customizable Risk Profiles:** Tailor danger thresholds and warning weights based on industry-specific compliance requirements (GDPR, HIPAA, CCPA).
- [ ] 🔌 **API & CI/CD Integrations:** Automated policy compliance checks for software dependencies and vendor agreements.

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" width="100%"/>

## 📜 License

Distributed under the **MIT License**. See `LICENSE` for more information. 💚

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=150&section=footer&text=Built%20with%20🤝%20transparency,%20⚡%20speed%20&%20🛡️%20trust&fontSize=24&fontAlignY=55&animation=twinkling" width="100%"/>



</div>
