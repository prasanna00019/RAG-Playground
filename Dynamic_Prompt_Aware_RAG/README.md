# 🧠 Dynamic Prompt-Aware RAG System using LlamaIndex

This project showcases a Retrieval-Augmented Generation (RAG) pipeline built with [LlamaIndex](https://www.llamaindex.ai/), enhanced with **dynamic prompt routing based on query tone or intent**. It demonstrates how a simple RAG setup can be evolved into an intelligent, user-aware system that responds in varying tones such as comparative, creative, elaborative, etc.

---

## 🔍 What is this project?

A document-based Q&A system that:
- Loads and indexes PDFs using embeddings
- Accepts user queries
- Dynamically detects the *tone* or *intent* of each query
- Routes it to an appropriate **custom prompt template**
- Performs RAG using the selected prompt and LLM
- Returns intelligent, context-aware answers

---

## 📈 Project Evolution

### ✅ Phase 1: Basic RAG with LlamaIndex
- Loaded documents from PDF
- Used `VectorStoreIndex` for retrieval
- Queried with `.query()` without custom prompt control
- Responses were generic and one-tone

### 🔥 Phase 2: Prompt-Augmented RAG
- Introduced `ResponseSynthesizer` to control prompt formatting
- Created custom `PromptTemplate`s for:
  - `compare`
  - `summarize`
  - `elaborate`
  - `creative`
  - `chat` (default fallback)

### 🚀 Phase 3: Dynamic Prompt Routing
- Built a lightweight **tone/intent classifier**
- Used LLM to classify user query type
- Dynamically selected the appropriate prompt template
- Created modular query flow: classify → route → synthesize → answer

---

## 🧠 Features

- 📄 PDF ingestion + embedding (Google GenAI or HuggingFace)
- 🔍 Semantic search using Chroma vector store
- 🧩 Custom response synthesis with prompt control
- 🔄 Tone-aware query classification via LLM
- 🎯 Dynamic RAG with prompt routing
- ✨ Clean, modular architecture for easy extension

---

## 🖼️ Prompt Types Used

| Prompt Type | Example Query |
|-------------|---------------|
| `compare`   | "Compare top-k and top-p sampling" |
| `summarize` | "List the key prompting techniques in the paper" |
| `elaborate` | "Explain chain-of-thought reasoning in detail" |
| `creative`  | "Describe prompt engineering using a cooking recipe analogy" |
| `chat`      | "What is prompt engineering?" |

---

## 📦 Tech Stack

- 🧠 **LlamaIndex** – RAG backbone
- ✍️ **Google GenAI** – LLM & embeddings (Gemini)
- 🧠 **PromptTemplate** + `ResponseSynthesizer` – Prompt control
- 📚 **Chroma** – Vector store backend
- 📄 **PyMuPDF** – PDF text parsing
- 🧪 **Python** – Language of choice

---

#Built with love, curiosity, and a passion for building better AI Apps
Thanks to [LlamaIndex](https://www.llamaindex.ai/) and open-source tools for making this powerful system possible.


