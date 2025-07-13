# 🧠 HyQe RAG: Hypothetical Query Embedding Retrieval-Augmented Generation

This project implements the **HyQe RAG** (Hypothetical Query Embedding Retrieval-Augmented Generation) technique, inspired by and following the methodology described in the research paper:  
[HyQe: Hypothetical Query Embeddings for Enhanced Retrieval-Augmented Generation](https://arxiv.org/pdf/2410.15262) 📄.

---

## 🚀 Overview

**HyQe RAG** enhances traditional RAG pipelines by generating hypothetical queries for each document chunk, embedding them, and using these embeddings to improve retrieval relevance. This approach enables more robust and context-aware retrieval, especially for complex or ambiguous user queries.

---

## 🛠️ Implementation Details

- **Document Loading & Splitting:**  
    Documents are loaded from the `data` directory and split into manageable chunks using a sentence splitter.

- **Embedding Models:**  
    - Uses Google GenAI for both LLM (for hypothetical query generation) and embedding models.
    - Embeddings are generated for both user queries and hypothetical queries.

- **Hypothetical Query Generation:**  
    For each document chunk, the LLM generates diverse, short hypothetical questions that could be answered by the chunk. These are then embedded and paired with their source chunk.

- **Retrieval & Re-ranking:**  
    - At query time, the user query is embedded.
    - Each document chunk is scored based on its original retrieval score and its maximum similarity to any of its hypothetical queries.
    - Chunks are re-ranked using a weighted combination of these scores.

- **Answer Generation:**  
    The top-ranked chunks are used as context for the LLM to generate a final answer.

---

## 📦 Key Features

- **Enhanced Retrieval:**  
    By leveraging hypothetical queries, the system retrieves more relevant and contextually appropriate chunks.

- **Plug-and-Play:**  
    Easily adaptable to different embedding models and LLMs.

- **Caching:**  
    Embedding pairs are cached for efficiency.

---

## 📋 Usage

1. **Configure API Keys:**  
     Set your Google API key in the environment.

2. **Load and Index Documents:**  
     Documents are loaded, split, and indexed with hypothetical query embeddings.

3. **Query:**  
     Enter a natural language question. The system retrieves, re-ranks, and generates an answer using the HyQe RAG pipeline.

---

## 📚 Reference

This implementation is directly inspired by and follows the methodology from:  
**HyQe: Hypothetical Query Embeddings for Enhanced Retrieval-Augmented Generation**  
[https://arxiv.org/pdf/2410.15262](https://arxiv.org/pdf/2410.15262)

---

## ✨ Acknowledgements

- Thanks to the authors of the HyQe paper for their innovative approach.
- Built using [LangChain](https://python.langchain.com/), [LlamaIndex](https://www.llamaindex.ai/), and Google GenAI APIs.

---

> 💡 **Note:** This notebook is a research-inspired implementation and may require further tuning for production use.  
> For more details, see the referenced paper above.