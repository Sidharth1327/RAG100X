## 🚀 Day 14 of RAG100x — Fusion-Based Retrieval (BM25 + Vector Search)

**📅 Date:** July 31, 2025  
**🎯 Goal:** Improve document retrieval quality by combining **semantic vector search** with **keyword-based BM25** retrieval using a score-level fusion strategy.

### ✅ What Was Built

- Created a **BM25 index** from tokenized documents using `rank_bm25`.  
- Integrated **FAISS-based vector retriever** for semantic similarity search.  
- Built a `fusion_retrieval()` function that:  
  - Performs both keyword and vector search  
  - **Normalizes scores** from each source  
  - **Combines them using a weighted average (alpha blending)**  
  - Returns the top-K most relevant documents based on fused scores.  

### 🧠 What I Learned

- **BM25** is effective for **lexical match** but may miss semantically similar content.  
- **Vector search** captures deeper meaning but can overlook exact keywords.  
- **Fusion retrieval** improves balance — combining strengths of both worlds.  
- Careful **score normalization** is crucial to fairly mix scores from two different models.  
- The fusion weight **alpha** controls the bias toward vector (semantic) or BM25 (lexical).

### 📊 Key Results

| Method            | Strengths                            | Weaknesses                          |
|------------------|--------------------------------------|-------------------------------------|
| BM25 Only        | Great for keyword match               | Misses paraphrased or semantic cues |
| Vector Only      | Captures meaning, paraphrases         | Ignores exact token matches         |
| **Fusion**       | Best of both — balanced and accurate  | Slightly more compute per query     |

### 🛠️ Stack Used

- **FAISS**, **rank_bm25**, **LangChain**, **NumPy**, **OpenAI**, **Colab**

---
