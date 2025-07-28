## 🚀 Day 3 of RAG100x — Web RAG with Source Attribution & Hallucination Detection

**📅 Date:** July 18, 2025   
**🎯 Goal:** Build a web-sourced RAG pipeline using blog data, LLaMA-3, Chroma, and Groq — with relevance grading and hallucination detection.

### ✅ What Was Built

- Scraped and parsed blog articles from DeepLearning.ai into LangChain `Document` objects.
- Embedded the content using Cohere’s `embed-english-v3.0` model and stored them in a Chroma vectorstore.
- Built a retriever with metadata filtering and semantic similarity for fetching relevant content.
- Used Groq’s Mixtral + structured output to filter irrelevant docs via a binary relevance grader.
- Constructed a `format_docs()` function to render full document metadata inline with generations.
- Generated concise, grounded answers using Groq’s LLaMA-3.1 (8B-Instant).
- Detected hallucinations by comparing generations with the retrieved context using a structured hallucination grading prompt.

### 🧠 What I Learned

- How to turn scraped web content into a structured, searchable vectorstore with source metadata.
- Why filtering retrieved chunks using a relevance grader boosts answer precision.
- How `structured_output()` in LangChain makes grading tasks easier with Pydantic models.
- Best practices for formatting input context for traceable source attribution.
- How to use a hallucination grader prompt to simulate grounding checks in the absence of gold answers.

### 🛠️ Stack Used

- LangChain, Chroma, Cohere Embeddings, Groq (Mixtral + LLaMA 3.1), Pydantic, Colab

---
