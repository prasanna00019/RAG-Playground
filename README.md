# RAG-Playground

A curated collection of RAG (Retrieval-Augmented Generation) projects covering foundational to advanced techniques, including prompt routing, agentic reasoning, and HyDe-style retrieval.

## 🗂️ Projects Overview

| Project Name                  | Description                                                                                   | Techniques Used                                                        | Link                             |
| ----------------------------- | --------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------- | -------------------------------- |
| **Dynamic Prompt-Aware RAG**  | Routes user queries to the best prompt template based on intent (e.g., summarize, compare).   | Prompt routing, LLM-based intent classification, LlamaIndex            | [View](Dynamic_Prompt_Aware_RAG) |
| **Agentic Multi-Doc RAG**     | Agent breaks query into sub-questions and retrieves from relevant document-specific indices.  | ReAct agent, query decomposition, per-doc vector indices, web fallback | [View](Multi_Doc_Agentic_RAG)    |
| **HyDe RAG (Single + Multi)** | Generates hypothetical answers to improve retrieval; supports single and multi-doc averaging. | Hypothetical generation, embedding reranking, dot product similarity   | [View](HyDe_RAG)                 |
| **Corrective RAG**            | Enhances answer reliability by verifying and correcting initial RAG output. Involves an evaluator agent that scores document relevance, a query rewriter for web fallback, and a generator that produces final answers from refined knowledge. Adapts dynamically based on confidence scoring (`CORRECT`, `INCORRECT`, `AMBIGUOUS`). | Evaluator agent (embedding + LLM), knowledge strip refinement, LLM query rewriting, web search fallback, generator agent | [View](Corrective_RAG)           |
| **HyPe RAG**                  | Improves retrieval by indexing hypothetical questions instead of chunk embeddings. Transforms query–document matching into query–question matching for better alignment with natural user queries. | Precomputed hypothetical prompts, dense embedding index (FAISS), prompt-to-prompt retrieval, LlamaIndex/FAISS integration | [View](HyPe_RAG)                 |
|**HyQe RAG**                   |  Enhances traditional RAG pipelines by generating hypothetical queries for each document chunk, embedding them, and using these embeddings to improve retrieval relevance                      |     Cosine similarity, Re-Ranking, Query to Query matching    | [View](HyQe_RAG)                 |
| **Self RAG** | Dynamically decides whether to use retrieved information and how to best utilize it in generating responses, aiming to produce more accurate, relevant, and useful outputs. | Retrieval decision, context filtering, support & utility scoring, prompt-based critique | [View](Self_RAG) |
|**Fusion RAG** | Leverages multiple query reformulations, document retrieval, and robust re-ranking to generate high-quality, contextually rich responses using LLMs | Re-Ranking(RRF score), Query Reformulation |[View](Fusion_RAG)
|**RAPTOR RAG** |  Organizes document chunks into a hierarchical tree using recursive clustering and abstractive summarization | Gausian Mixture Model(GMM), semantic chunking | [View](RAPTOR_RAG)
|**Knowledge Graph RAG** | Builds knowledge graph over the data and gives context aware responses | Graph data structure  |[View](KG_RAG) 
---

> Built with ❤️ for scalable, modular experimentation in the world of RAG.
