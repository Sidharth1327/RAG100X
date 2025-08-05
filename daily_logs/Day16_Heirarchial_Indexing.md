## 🚀 Day 16 of RAG100x — Hierarchical Retrieval with Summary-Guided Filtering

**📅 Date:** August 5, 2025  
**🎯 Goal:** Improve relevance in long-document retrieval by implementing **two-tiered retrieval** — summaries first, then detailed chunks scoped by summary context.

### ✅ What Was Built

- Implemented a **hierarchical retrieval pipeline** using two separate FAISS vectorstores:  
  - One for **document-level summaries**  
  - One for **fine-grained detailed chunks**
- Encoded and stored PDF content into these stores using **OpenAI Embeddings**.  
- Created a **filtering mechanism** to match detailed chunks with their associated summary based on **page numbers**.  
- Final retrieval flow:  
  1. Retrieve top-K summaries  
  2. Filter detailed chunks linked to those summaries  
  3. Return the top-N matching detailed chunks to the LLM

### 🧠 What I Learned

- **Hierarchical retrieval** mimics how humans search — first skimming, then diving deeper.  
- Page-based **metadata filtering** keeps the second-stage retrieval focused and fast.  
- Helps reduce noisy or off-topic context from being fed into the LLM.  
- Works particularly well for **lengthy PDFs** where broad vector search alone introduces semantic drift.  
- Can be combined later with **CrossEncoder reranking** for even greater precision.

### 📊 Key Results

| Stage                        | Purpose                             | Trade-offs                                |
|-----------------------------|-------------------------------------|-------------------------------------------|
| Summary-Level Retrieval     | Identify relevant regions quickly   | Risk of missing detail if summaries are vague |
| Detailed Chunk Filtering    | Focus retrieval within top summaries| Requires clean metadata (e.g., page numbers) |
| Combined Hierarchical Flow  | Better targeted context for LLM     | Slightly more complex retrieval logic     |

### 🛠️ Stack Used

- **FAISS**, **OpenAI Embeddings**, **LangChain**, **sentence-transformers**, **Colab**

---
