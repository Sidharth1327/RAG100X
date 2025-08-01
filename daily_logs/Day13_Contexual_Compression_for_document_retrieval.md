## 🚀 Day 13 of RAG100x — Contextual Compression for Focused Retrieval

**📅 Date:** July 30, 2025  
**🎯 Goal:** Improve retrieval precision by **compressing retrieved documents** to include only the most relevant parts using an LLM-based contextual compressor.

### ✅ What Was Built

- Created a **FAISS-based retriever** to pull top-k relevant chunks from a document.  
- Implemented **LLMChainExtractor** using `gpt-4o-mini` to extract high-salience segments.  
- Combined retriever + compressor using **ContextualCompressionRetriever** from LangChain.  
- Built a **RetrievalQA chain** that only receives compressed (filtered) content for generation.  
- Tested with a sample query: *"What was the impact of the Paris Climate Agreement?"*

### 🧠 What I Learned

- Full retrieved chunks can contain **a lot of irrelevant filler**, which hurts LLM response quality.  
- **Contextual compression** is like a "salience filter" — only the most useful content is retained.  
- Using GPT-4o-mini as the compressor keeps the process lightweight yet semantically strong.  
- The architecture is modular — you can **swap in different compressors or retrievers** easily.

### 📊 Key Results

| Metric                        | Without Compression            | With Compression                        |
|------------------------------|--------------------------------|------------------------------------------|
| Context length               | Full chunk (500+ tokens avg)   | ~150-250 tokens after filtering          |
| Relevance of answers         | Sometimes diluted              | More focused and precise                 |
| Cost & latency               | Higher                         | Reduced due to trimmed input             |

### 🛠️ Stack Used

- **LangChain**, **OpenAI (GPT-4o-mini)**, **FAISS**, **LLMChainExtractor**, **ContextualCompressionRetriever**, **Colab**

---
