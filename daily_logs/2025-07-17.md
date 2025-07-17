## 🚀 Day 2 of RAG100x — CSV → QA RAG System

**📅 Date:** July 17, 2025  
**📂 Notebook:** `02_csv_qa_rag.ipynb`  
**🎯 Goal:** Build a simple but complete CSV-powered QA RAG system using FAISS + OpenAI embeddings.

### ✅ What Was Built

- Parsed structured CSV data into LangChain `Document` objects using `CSVLoader`.
- Converted tabular rows into semantic embeddings with OpenAI's `text-embedding-3-small`.
- Created a FAISS vector index to support similarity-based retrieval.
- Defined a `retriever` interface to fetch relevant rows based on a natural language query.
- Built a `retrieval → stuff → GPT-4o` pipeline using `create_retrieval_chain`.
- Enabled direct natural language Q&A over spreadsheet data — no schema, no SQL.

### 🧠 What I Learned

- How to repurpose structured CSV rows for semantic search.
- The role of LangChain’s `CSVLoader`, and why it returns rows as individual documents.
- Why `FAISS.from_documents()` is used for simple setups and when to go manual instead.
- Under-the-hood flow of `create_retrieval_chain`: retrieval ➝ stuffing ➝ generation.
- That chunking *does* happen even in CSVs — one row = one chunk in this context.

### 🛠️ Stack Used

- LangChain, FAISS, OpenAI, Colab

---
