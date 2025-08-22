## 🚀 Day 17 of RAG100x — GraphRAG with Knowledge Graph Traversal

**📅 Date:** August 7, 2025  
**🎯 Goal:** Enhance retrieval by building a **knowledge graph** from documents, enabling multi-hop reasoning and more interpretable RAG responses.

### ✅ What Was Built

- Developed a **GraphRAG pipeline** with these key components:  
  - **KnowledgeGraph**: extracts entities & relationships, storing them as nodes and edges.  
  - **GraphRAG**: central class combining LLM, embeddings, graph building, vector search, and querying.  
  - **QueryEngine**: hybrid approach using both **vector retrieval** and **graph traversal**.  
  - **Visualizer**: renders traversal paths, making reasoning steps transparent.  
- Implemented retrieval flow:  
  1. Extract entities/relationships → build knowledge graph  
  2. Perform vector search for semantically close chunks  
  3. Traverse related graph nodes to enrich context  
  4. Generate structured and interpretable answers  

### 🧠 What I Learned

- Graph-based retrieval goes **beyond embeddings**, capturing how concepts connect.  
- Traversal allows **multi-hop reasoning**, crucial for research/technical/legal use cases.  
- Visualization adds **interpretability**, showing *why* an answer was retrieved.  
- Hybrid retrieval (vector + graph) balances semantic similarity with structured knowledge.  
- Useful when **relationships matter as much as content** — unlike plain chunk matching.  

### 📊 Key Results

| Stage                     | Purpose                                   | Trade-offs                              |
|----------------------------|-------------------------------------------|------------------------------------------|
| Knowledge Graph Building   | Capture entities & relationships          | Dependent on extraction quality          |
| Vector Retrieval           | Find semantically similar text quickly    | Can miss multi-hop or cross-concept links|
| Graph Traversal            | Link related facts for deeper reasoning   | More compute overhead on large graphs    |
| Hybrid Querying            | Blend semantic + relational retrieval     | Slightly more complex orchestration      |

### 🛠️ Stack Used

- **LangChain**, **FAISS**, **NetworkX**, **OpenAI LLMs + Embeddings**, **Matplotlib** (for visualization), **Colab**

---
