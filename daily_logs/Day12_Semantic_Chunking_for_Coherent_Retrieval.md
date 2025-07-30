## 🚀 Day 12 of RAG100x — Semantic Chunking for Coherent Retrieval

**📅 Date:** July 30, 2025  
**🎯 Goal:** Improve retrieval quality by **splitting documents at semantically meaningful points**, rather than fixed sizes, using embedding-based chunking.

### ✅ What Was Built

- Implemented **SemanticChunker** from LangChain with OpenAI embeddings.  
- Explored three chunking strategies: **percentile**, **standard deviation**, and **interquartile range**.  
- Used the **90th percentile** of semantic distance between sentence embeddings to detect chunk boundaries.  
- Created a **FAISS vectorstore** with semantically coherent chunks for downstream retrieval.  
- Ran a retrieval example query: *"What is the main cause of climate change?"*

### 🧠 What I Learned

- Semantic distances between sentence embeddings can **accurately detect idea shifts** in text.  
- **Percentile-based breakpoints** allow control over chunk granularity with intuitive thresholds.  
- Chunks created this way are **more complete and self-contained**, helping retrieval performance.  
- LLMs respond better when provided with **full-context chunks** rather than fragmented ones.

### 📊 Key Results

| Scenario                      | Fixed-size Chunking           | Semantic Chunking                     |
|-------------------------------|-------------------------------|----------------------------------------|
| Chunk coherence               | Often cuts across sentences   | Preserves full thoughts and structure  |
| Retrieval relevance           | Matches tokens, not meaning   | Matches intent more precisely          |
| Implementation complexity     | Simple but rigid              | Flexible and embedding-aware           |

### 🛠️ Stack Used

- **LangChain**, **OpenAI (Embeddings + GPT-4o)**, **FAISS**, **SemanticChunker**, **Colab**

---
