## 🚀 Day 4 of RAG100x — Evaluation-Driven RAG Benchmarking (Faithfulness + Relevance)

**📅 Date:** July 19, 2025  
**🎯 Goal:** Build an evaluation-focused RAG system using LlamaIndex and OpenAI to measure how chunk size affects response quality and latency.

### ✅ What Was Built

- Loaded plain text documents using LlamaIndex’s `SimpleDirectoryReader`.
- Generated a set of evaluation questions from the documents using `DatasetGenerator`.
- Designed an automated evaluation pipeline to:
  - Retrieve and generate answers from a custom RAG chain
  - Score each answer for **faithfulness** and **relevancy** using structured graders
  - Track average response time per chunk size
- Benchmarked performance using two chunk sizes: 128 and 256 tokens.
- Analyzed how chunking granularity affects generation quality and speed.

### 🧠 What I Learned

- How to build a minimal RAG system using LlamaIndex's new `ComposableGraph` and `QueryEngine`.
- The usefulness of structured LLM outputs for auto-grading generation quality.
- Why larger chunks (e.g., 256 tokens) may improve inference speed without hurting faithfulness or relevance.
- How `ServiceContext` and `Settings` provide control over chunking and LLM configuration.
- How to simulate production-style evaluations without gold answers by leveraging GPT-4 as a grader.

### 📊 Evaluation Results

| Chunk Size | Avg. Response Time | Faithfulness | Relevancy |
|------------|--------------------|--------------|-----------|
| **128**    | 1.35 sec           | ✅ 1.00       | ✅ 1.00    |
| **256**    | 1.31 sec           | ✅ 1.00       | ✅ 1.00    |

### 🛠️ Stack Used

- **LlamaIndex**, **OpenAI GPT-4**, **Pydantic**, **Python Standard Library**, **Colab**

---
