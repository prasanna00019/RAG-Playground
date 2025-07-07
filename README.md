# RAG-Playground
A comprehensive collection of RAG (Retrieval Augmented Generation) implementations 📚✨, from foundational concepts to advanced agentic 🤖 and knowledge graph 🌐 RAGs
---

## 📌 Featured Project: Dynamic Prompt-Aware RAG

Explore my **first RAG project**, where I started with basic LlamaIndex retrieval and evolved it into a **tone-aware, prompt-routed RAG system**.

🧠 It dynamically detects the intent of user queries — such as compare, summarize, elaborate, or creative — and routes them to the appropriate prompt template using LLM-based classification.

👉 [View Project File → dynamic_aware_rag.ipynb](Dynamic_Prompt_Aware_RAG)

---

## 🚀 New Project: Agentic Multi-Document RAG

Dive into my **second RAG project**, where I build a powerful **AI agent that intelligently navigates multiple document sources**.

🧠 Instead of combining all documents into a single vector store, I maintain **separate chunked vector indices** for each document type (like AWS Lambda, EC2, etc.).

🤖 The agent performs:
- Query decomposition using `break_question`
- Document classification using `classify_user_query`
- Intelligent retrieval from the correct document engine(s) using `RUN_RAG`
- Optional web fallback with `search_web`
- Step-by-step reasoning using the ReAct framework

⚡ This modular architecture is **more efficient and scalable** than traditional monolithic RAG setups and mimics real-world QA systems.

👉 [View Project File → Multi_Doc_Agentic_RAG.ipynb](Multi_Doc_Agentic_RAG)

---