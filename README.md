# 🧾 **Legal AI Assistant – Making Indian Law Accessible with AI**

---

## 📌 **Problem Statement**

Accessing accurate legal information in India remains a persistent challenge. Citizens and even early-career legal professionals face two major obstacles: **constitutional illiteracy** and **procedural complexity**. Questions like *"What is Article 21?"* require precise constitutional knowledge, while queries like *"How do I file for bail?"* demand guidance rooted in real-world legal procedures and case law.

Traditional search engines return generic results, and legal help is often unaffordable or inaccessible. Most existing AI tools are either not trained on Indian law or fail to distinguish between factual and procedural queries, leading to superficial or inaccurate answers.

General-purpose LLMs like GPT or Claude lack access to current legal documents, verdicts, or precedents, and cannot retrieve live case law — making them unsuitable for practical legal assistance.

---

## ✅ **Solution Overview**

The **Legal AI Assistant** bridges this gap through a **hybrid AI system** that combines deep constitutional knowledge with real Supreme Court case precedents. Built on **IBM Granite models**, it detects the nature of a legal question and chooses between:
- A **fine-tuned model** for fast, accurate constitutional answers
- A **RAG (Retrieval-Augmented Generation) pipeline** to search and cite relevant case law

This **fusion architecture** ensures users receive the correct legal perspective—**theoretical understanding** or **practical application**—with **citations for every response**.

---

## 🧑‍⚖️ **Target Users & Interaction**

**Primary Users:**
- Citizens seeking legal clarity  
- Law students and junior lawyers  
- NGOs and legal aid workers

**Interaction:**
Users interact via a simple **chat interface**. Queries are routed to the appropriate backend:
- Fine-tuned QA model
- RAG pipeline retrieving from 88,000+ Supreme Court case chunks

Users can also request **comparison mode** to view both constitutional and case-based interpretations.

---

## 🚀 **What Makes It Unique**

### 🔁 **Fusion of Models**
Uses intelligent routing between:
- **Granite 3.3-8B** fine-tuned on 14,543 QA pairs (Constitution, IPC, CrPC)
- **Granite-powered RAG system** for real-time case law retrieval

### 📚 **Case-Law Grounded Answers**
Provides procedural/legal responses backed by actual case citations — a feature absent in general AI models.

### 🔗 **Smart Citation and Trust**
Every response includes **verifiable citations** with access to source documents — increasing legal transparency and reliability.

---

## 🧠 **AI Innovation & Efficiency**

- LoRA-based fine-tuning on Indian legal QA
- Granite 30M embeddings with FAISS vector search
- 85%+ accurate **query classifier**
- **Sub-2 second response times**
- Scalable to include PIL, RTI, state-level legal frameworks

---

## 📊 **Impact**

Our assistant actively incorporates real case law and contextual understanding of procedural history. It **reduces legal research time** from hours to seconds, empowers legal literacy, and democratizes access across India’s diverse legal system.

---

## 🏛️ **IBM Granite Usage in Legal AI Assistant**

Our **Legal AI Assistant** is fundamentally built on **IBM Granite models**, integrated across three core components that leverage the model family’s enterprise-grade capability for domain-specialized tasks in Indian law.

---

### 🔹 **1. Fine-Tuned Text Generation with Granite 3.3-8B Instruct**

- **Model Used**: `ibm-granite/granite-3.3-8b-instruct`
- **Implementation**: Applied **LoRA (Low-Rank Adaptation)** fine-tuning on **14,543 Indian legal QA pairs** from the Constitution, CrPC, and IPC datasets.
- **Training Configuration**:
  - Epochs: 5
  - Learning Rate: `2e-4`
  - PEFT: Parameter-Efficient Fine-Tuning
  - Quantization: 4-bit loading for memory optimization
- **Specialization**:
  - Designed for answering direct constitutional queries like *"What is Article 21?"*
  - Produces precise definitions and legally accurate summaries
  - Maintains Granite’s safety and robustness
  - Utilizes Granite’s chat template format: `<|system|>`, `<|user|>`, `<|assistant|>`

---

### 🔹 **2. Legal Document Embeddings with Granite 30M English**

- **Model Used**: `ibm-granite/granite-embedding-30m-english`
- **Implementation**:
  - Vectorized over **88,000 document chunks** from Indian Supreme Court judgments
  - Converts legal texts into semantic embeddings optimized for similarity search
  - Enables high-recall document retrieval using **FAISS (cosine similarity)**
- **Chunking Strategy**:
  - Size: 1000 characters
  - Overlap: 200 characters
- **Corpus**: Cleaned case text files like `C1001.txt`, `C2040.txt`, etc.

---

### 🔹 **3. RAG-Enhanced Generation Pipeline**

- Combines both Granite models in a **RAG (Retrieval-Augmented Generation)** architecture.
- **Workflow**:
  ```text
  User Query → Embedding via Granite 30M →
  FAISS Search → Retrieve Top-k Case Chunks →
  Input to Fine-Tuned Granite 3.3-8B →
  Output: Context-aware Legal Answer with Citations

## 🖼️ **System Overview Diagram**

![System Architecture](https://github.com/gadhalekshmip/LawChat/raw/main/mermaid.png)

> *Above: Mermaid diagram showing query classification, Granite model routing, and case-law retrieval pipeline.*
---

## 🎥 **Demo Video**

[![Watch the Demo Video](https://img.youtube.com/vi/y7fpiCfJscg/hqdefault.jpg)](https://www.youtube.com/watch?v=y7fpiCfJscg)

> *Click the thumbnail above to see the Legal AI Assistant in action.*

---







