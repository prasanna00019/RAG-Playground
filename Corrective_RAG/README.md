# 🧠 Corrective RAG (CRAG) Implementation from Scratch

Welcome to this notebook! Here, you'll find a **from-scratch implementation** of the Corrective RAG (CRAG) framework, inspired by the research paper:  
[Corrective RAG: Faithful and Efficient Retrieval-Augmented Generation via Corrective Reasoning](https://arxiv.org/pdf/2401.15884)

---

## 🚀 What is Corrective RAG?

Corrective RAG (CRAG) is an advanced Retrieval-Augmented Generation (RAG) approach that enhances factual accuracy and reliability in LLM-based question answering. It introduces a **corrective reasoning loop** that verifies, refines, and supplements retrieved knowledge before generating a final answer.

---

## 🛠️ Implementation Highlights

- **Built from scratch**: No high-level CRAG libraries used—every component is custom-coded for transparency and flexibility.
- **Google Gemini & Embeddings**: Uses `langchain-google-genai` and `llama_index.embeddings.google_genai` for LLM and embedding models.
- **Vector Store Indexing**: Documents are split, embedded, and indexed for efficient retrieval.
- **Factuality Evaluation**: Combines similarity scoring and LLM-based factual checks to classify answers as `CORRECT`, `INCORRECT`, or `AMBIGUOUS`.
- **Web Search Integration**: For ambiguous or incorrect cases, queries are rewritten and external web search is performed (via Serper API).
- **Knowledge Refinement**: Retrieved passages are split into fine-grained "knowledge strips" and filtered for relevance using the LLM.
- **Final Answer Generation**: The LLM generates a response strictly based on the refined internal and/or external knowledge.

---

## 📂 Project Structure

- **Document Loading & Indexing**: Loads documents from the `data/` directory, splits them into nodes, and builds a vector index.
- **Factuality Agent**: Evaluates if retrieved passages support the query, invoking LLM checks when uncertain.
- **Query Rewriting & Web Search**: Rewrites queries for optimal web search and fetches up-to-date information.
- **Knowledge Refinement**: Extracts and recomposes only the most relevant knowledge strips for answer generation.
- **CRAG Inference Pipeline**: Orchestrates the above steps to deliver factually accurate and context-aware answers.

---

## 📊 Example Usage

- Ask a question like:  
    *"What is the difference between Flat white and cappuccino?"*
- The system retrieves, verifies, and refines knowledge, then generates a grounded answer.
- If internal knowledge is insufficient, it automatically supplements with web search.

---
## CITATION 
```bibtex
@misc{yan2024correctiveretrievalaugmentedgeneration,
      title={Corrective Retrieval Augmented Generation}, 
      author={Shi-Qi Yan and Jia-Chen Gu and Yun Zhu and Zhen-Hua Ling},
      year={2024},
      eprint={2401.15884},
      archivePrefix={arXiv},
      primaryClass={cs.CL},
      url={https://arxiv.org/abs/2401.15884}, 
}
```
---

## 📖 References

- [Corrective RAG Paper (arXiv:2401.15884)](https://arxiv.org/pdf/2401.15884)

---

## 💡 Get Started

1. Place your documents in the `data/` folder.
2. Set your API keys for Google and Serper.
3. Run the notebook cells in order.
4. Try your own queries and explore the corrective reasoning process!

---

**Happy experimenting with CRAG!** 🦾✨