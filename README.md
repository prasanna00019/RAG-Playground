# RAG-Playground

A curated collection of RAG (Retrieval-Augmented Generation) projects covering foundational to advanced techniques, including prompt routing, agentic reasoning, and HyDe-style retrieval.

## 🗂️ Projects Overview

| Project Name                  | Description                                                                                   | Techniques Used                                                        | Link                             |
| ----------------------------- | --------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------- | -------------------------------- |
| **Dynamic Prompt-Aware RAG**  | Routes user queries to the best prompt template based on intent (e.g., summarize, compare).   | Prompt routing, LLM-based intent classification, LlamaIndex            | [View](Dynamic_Prompt_Aware_RAG) |
| **Agentic Multi-Doc RAG**     | Agent breaks query into sub-questions and retrieves from relevant document-specific indices.  | ReAct agent, query decomposition, per-doc vector indices, web fallback | [View](Multi_Doc_Agentic_RAG)    |
| **HyDe RAG (Single + Multi)** | Generates hypothetical answers to improve retrieval; supports single and multi-doc averaging. | Hypothetical generation, embedding reranking, dot product similarity   | [View](HyDe_RAG)                 |

---

> Built with ❤️ for scalable, modular experimentation in the world of RAG.
