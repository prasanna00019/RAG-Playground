# 🧠 Hypothetical Prompt Embedding RAG (HyPE) - Q2Q Retrieval

Welcome to the **Hypothetical Prompt Embedding RAG** project!  
This notebook demonstrates an advanced Retrieval-Augmented Generation (RAG) workflow using **Hypothetical Prompt Embeddings (HyPE)**, inspired by recent research.

---

## 🚀 What is HyPE?

Traditional RAG systems retrieve document chunks based on query-to-document similarity.  
**HyPE** takes a novel approach:  
- For each document chunk, it generates a set of *hypothetical questions* that the chunk could answer.
- At query time, the user’s question is embedded and matched **directly to these hypothetical questions** (Q2Q matching), rather than to the original document text.

This leads to more precise and contextually relevant retrieval, bridging the gap between user queries and document content.

---

## 🛠️ How It Works

1. **Document Chunking:**  
    Documents are split into manageable chunks.

2. **Hypothetical Question Generation:**  
    For each chunk, an LLM generates essential questions that the chunk could answer.

3. **Embedding:**  
    Both hypothetical questions and user queries are embedded using a powerful embedding model.

4. **Q2Q Retrieval:**  
    At query time, the user’s question is matched against the pool of hypothetical questions using vector similarity (cosine/FAISS).

5. **Answer Generation:**  
    The most relevant chunks are used as context for the LLM to generate a final answer.

---

## 📦 Features

- End-to-end HyPE pipeline implemented from scratch
- Uses Google Gemini and Google Embeddings
- Supports both brute-force and FAISS-based retrieval
- Modular and extensible code

---

## 📖 References

- **Bridging the Question-Answer Gap in Retrieval-Augmented Generation: Hypothetical Prompt Embeddings**  
  [Research Paper Link](https://www.researchgate.net/publication/389032824_Bridging_the_Question-Answer_Gap_in_Retrieval-Augmented_Generation_Hypothetical_Prompt_Embeddings)

---

## ✨ Credits

This project is implemented from scratch, inspired by the above paper.  
All code and logic are original and tailored for educational and research purposes.

---

Happy experimenting! 🤖✨