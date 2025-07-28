📅 2025-07-15 — Day 1 Log
What I built today:

Set up the project structure: rag_techniques/, notebooks/, utils/, assets/, daily_logs/

Implemented a basic PDF-based RAG pipeline in Colab (self-contained)

Wrote helper functions inline: encode_pdf, retrieve_context_per_question, replace_t_with_space, etc.

Connected OpenAI API (although quota error 😢)

Clean markdown explanations added for every section of the notebook

Added a summary cell and evaluation hook

Learnings:

Understood the end-to-end flow of basic RAG

Understood LangChain components like RecursiveCharacterTextSplitter, FAISS, and OpenAIEmbeddings

Understood trade-offs in keeping code self-contained vs modular

Next steps:

Add support for HuggingFace embeddings as an OpenAI alternative

Explore hybrid retrieval (BM25 + dense vectors)