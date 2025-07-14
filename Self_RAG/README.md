# 🤖 Self-RAG 

Welcome to the **Self-Retrieval-Augmented Generation (Self-RAG)** project!  
This notebook demonstrates a workflow inspired by the [Self-RAG paper (arXiv:2310.11511)](https://arxiv.org/pdf/2310.11511), where a language model decides **when and how** to retrieve external knowledge to answer queries more effectively.

---

## 🚀 Overview

- **Self-RAG** enables an LLM to:
    - Decide if external retrieval is needed for a given query.
    - Retrieve relevant documents using a vector store.
    - Filter and retain only the most relevant context.
    - Generate answers using either retrieved context or internal knowledge.
    - Evaluate the factual support and usefulness of generated responses.

---

## 🛠️ Workflow

1. **API Key Setup**  
     Securely input your API keys for Groq and Google.

2. **Model Initialization**  
     - Uses `langchain-groq` and `langchain-google-genai` for LLMs.
     - Uses Google GenAI embeddings for vector search.

3. **Document Loading & Indexing**  
     - Loads documents from the `data` directory.
     - Splits them into chunks and indexes them in a vector store.

4. **Self-RAG Pipeline**  
     - `retrieval_required`: Determines if retrieval is needed.
     - `is_context_relevant`: Filters retrieved chunks based on relevance.
     - `response_generation`: Generates answers using either context or model knowledge.
     - `support_response` & `utility_response`: 
       - Evaluate how well the generated answer is supported by context (if retrieved).
       - Always prints the **utility score** (even if no retrieval is used), as described in the Self-RAG paper.
     - `self_RAG`: Coordinates all the steps for each query.

5. **Example Queries**  
     - The notebook runs queries related to robotics and shows how Self-RAG handles them.

---

## 📦 Key Features

- **Dynamic Retrieval**: Avoids unnecessary lookups.
- **Context Filtering**: Keeps only what's truly relevant.
- **Answer Scoring**: Scores responses based on factual support and usefulness.
- **Modular Design**: Clean, reusable components.

---

## 📚 References

- [Self-RAG: Learning to Retrieve, Generate, and Critique in a Self-Refining Loop (arXiv:2310.11511)](https://arxiv.org/pdf/2310.11511)

---

## 💡 How to Use

1. Place your documents in the `data` folder.
2. Run the notebook cells sequentially.
3. Enter your API keys when prompted.
4. Run your own queries using the `self_RAG` function.

---

## 📝 Notes

- ⚠️ **This is not an exact reproduction of the Self-RAG paper**, but a simplified and practical implementation inspired by its core ideas.
- The current version avoids agentic loop structures and focuses on step-wise reasoning with modular functions.
- The **utility score is printed for every response**, even when no retrieval is performed, in alignment with the critique step in the paper.
- Feel free to adapt or extend it for your own use cases!


---

Happy experimenting! 🤗
