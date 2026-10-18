<div align="center">

# 📜 AgenticRAGreement
### *An Agentic RAG System with Human-in-the-Loop Agreement Governance*

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10%2B-blue?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Gradio-5.0%2B-orange?style=for-the-badge&logo=gradio&logoColor=white" alt="Gradio">
  <img src="https://img.shields.io/badge/Gemini_AI-2.5_Flash-purple?style=for-the-badge&logo=google&logoColor=white" alt="Gemini">
  <img src="https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge" alt="License">
  <img src="https://img.shields.io/badge/UI-3D%20Rainbow%20Glass-ff0055?style=for-the-badge" alt="UI Theme">
</p>

<p align="center">
  <b>Answers from your verified notes first. Intelligent Gemini AI fallback second. Complete human approval control always. ✋</b>
</p>

---
</div>

## 🌟 Overview

**AgenticRAGreement** is a next-generation, agentic Retrieval-Augmented Generation (RAG) assistant designed for rigorous contract, agreement, and policy document analysis. 

Unlike traditional black-box chatbots, AgenticRAGreement guarantees full transparency and security by checking your local verified knowledge base first using semantic vector search. If a query falls outside your verified documents, **Gemini AI** proposes a candidate answer—which is **only** written to your markdown vault and indexed upon your explicit approval.

---

## 🏗️ System Architecture & Workflow

The application operates on a robust, multi-stage agentic pipeline that ensures zero unverified data enters your persistent vault:

```mermaid
graph TD
    A[User Query Input] --> B[Sentence-Transformers Embedding]
    B --> C{Semantic Similarity Score >= 0.30?}
    C -- Yes --> D[📘 Retrieve Verified Local Note]
    C -- No --> E[🤖 Query Gemini AI Fallback]
    E --> F[✋ Present Approval Dialog to User]
    F -- Approved --> G[📝 Append to Markdown Vault & Re-index Instantly]
    F -- Rejected --> H[🗑️ Discard Candidate Draft]
    D --> I[Render Response in Chat UI]
    G --> I
