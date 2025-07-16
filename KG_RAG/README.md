# 🧠 Knowledge Graph RAG with LlamaIndex + Gemini (No Neo4j)

A lightweight, Neo4j-free implementation of **Knowledge Graph Retrieval-Augmented Generation (KG-RAG)** using:
- 🧾 LlamaIndex's `KnowledgeGraphIndex` + `SimpleGraphStore`
- 🔍 Google Gemini 2.5 + Gemini Embeddings (`text-embedding-004`)
- 📄 PDF document loader and triplet extractor
- 🕸 PyVis network visualization for the knowledge graph 
- 📬 Hybrid querying with graph context and custom prompting

---

## 📘 What is KG-RAG?

**KG-RAG** extends traditional RAG by retrieving structured **triplets (subject-predicate-object)** and building a **knowledge graph** over them. It enables more **context-aware, fact-checked, and explainable** answers from LLMs.

Unlike vector-only RAG, KG-RAG gives the LLM a **domain model** of the data — enabling logical reasoning, relationship understanding, and minimal hallucination.

---

## 🧰 Tech Stack

| Component        | Description                              |
|------------------|------------------------------------------|
| **LlamaIndex**   | For document parsing, graph indexing     |
| **Gemini 2.5**   | For LLM-based querying                   |
| **text-embedding-004** | For generating chunk-level embeddings |
| **SimpleGraphStore** | In-memory triple store (no Neo4j)      |
| **PyVis**        | Graph visualization                      |

---

## 🚀 How It Works

1. 📄 Load PDF document using `SimpleDirectoryReader`
2. 🧠 Split into chunks using `SentenceSplitter`
3. 🔍 Extract triplets (subject-predicate-object) via `KnowledgeGraphIndex`
4. 🗃️ Store triplets in an in-memory `SimpleGraphStore`
5. 🌐 Visualize the graph with PyVis 
6. 💬 Run a hybrid query with Gemini and display the answer

---