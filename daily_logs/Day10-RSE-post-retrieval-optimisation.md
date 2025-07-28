## 🚀 Day 10 of RAG100x — Relevant Segment Extraction (RSE)

**📅 Date:** July 29, 2025  
**🎯 Goal:** Go beyond top-k retrieval by identifying and extracting **coherent, high-relevance segments** from documents using a smoothed scoring mechanism.

### ✅ What Was Built

- Implemented a custom **relevance scoring function** based on GPT-4o similarity scores.  
- Built a **sliding window-based reranking pipeline** to evaluate chunk relevance in context.  
- Created a visualization for **chunk-wise similarity distribution** to inspect retrieval focus areas.  
- Developed an **optimization routine** to extract **non-overlapping, high-scoring segments** under size constraints.  
- Compared retrieved segments to top-k results and validated gains in semantic focus.

### 🧠 What I Learned

- Chunk-wise relevance often forms **local clusters**, which are missed by naive top-k retrieval.  
- Subtracting a small **irrelevance penalty** helps suppress noisy chunks without over-pruning.  
- Extracting segments via **greedy span optimization** improves retrieval coherence.  
- RSE works well with long, structured documents where related content is grouped.  
- Visualization helps identify which parts of the document the model finds relevant.

### 📊 Key Results

| Scenario                      | Top-k Retrieval                     | RSE-based Retrieval                      |
|-------------------------------|--------------------------------------|------------------------------------------|
| Chunk focus                   | Isolated, sometimes scattered        | Dense, coherent segment blocks           |
| Retrieval coherence           | Misses mid-doc sections              | Prioritizes focused, relevant areas      |
| Customization                 | Limited beyond `k`                  | Tunable via window, threshold, span size |

### 🛠️ Stack Used

- **LangChain**, **GPT-4o (ChatOpenAI)**, **FAISS**, **Matplotlib**, **Numpy**, **Custom RSE logic**, **Colab**

---
