## 🚀 Day 6 of RAG100x — Query Transformation for Better Retrieval

**📅 Date:** July 23, 2025  
**🎯 Goal:** Build a modular RAG pipeline that applies LLM-powered query transformation techniques — rewriting, step-back prompting, and sub-query decomposition — to improve retrieval precision and answer quality.

### ✅ What Was Built

- Implemented a **Query Rewriting Chain** using GPT-4o to rephrase vague queries into precise, retriever-friendly alternatives.  
- Added a **Step-back Prompting Chain** to expand narrow queries into broader contextual prompts that improve recall.  
- Created a **Sub-query Decomposition Chain** that breaks complex multi-hop questions into 2–4 simpler sub-queries.  
- Designed each transformation as a **composable LangChain LLMChain**, enabling modular use in different RAG pipelines.  
- Demonstrated each technique on an example query from the *Understanding Climate Change* dataset.  
- Ensured each transformation outputs **clean, ready-to-retrieve strings**, suitable for downstream FAISS or Chroma retrievers.  
- Prepared the pipeline for future integration with evaluation metrics like relevancy, faithfulness, and answer quality.

### 🧠 What I Learned

- Query quality plays a **foundational role in retrieval effectiveness** — better input leads to better context.  
- Different queries require different transformations — vague queries benefit from rewriting, while complex ones need decomposition.  
- Step-back prompting is powerful for **context enrichment**, especially when user queries assume hidden background knowledge.  
- Modularizing query transformations using LangChain chains makes the system **production-friendly and extensible**.  
- Clean prompts with few-shot examples significantly improve the **stability and interpretability** of LLM outputs.

### 📊 Key Results

| Technique                | When to Use                             | Strengths                              | Limitations                            |
|--------------------------|------------------------------------------|----------------------------------------|----------------------------------------|
| Query Rewriting          | Vague or underspecified queries          | Improves precision & intent clarity    | May miss context if over-trimmed       |
| Step-back Prompting      | Narrow or technical queries              | Adds helpful background & breadth      | Slightly less specific                 |
| Sub-query Decomposition  | Complex or multi-hop queries             | Increases coverage & completeness      | Needs multi-query aggregation later    |

### 🛠️ Stack Used

- **LangChain**, **ChatOpenAI (GPT-4o)**, **PromptTemplate**, **LLMChain**, **Python**, **Colab**

---
