# 🚀 Fusion RAG: Enhanced Retrieval-Augmented Generation

Welcome to the **Fusion RAG** project! This notebook demonstrates an advanced Retrieval-Augmented Generation (RAG) pipeline inspired by the [RAG-Fusion](https://arxiv.org/pdf/2402.03367) approach. The workflow leverages multiple query reformulations, document retrieval, and robust re-ranking to generate high-quality, contextually rich responses using Large Language Models (LLMs).

---

## 🧩 How It Works

1. **Query Reformulation**  
    For a user's input query, we generate _n_ semantically diverse sub-queries to cover different aspects of the information need.

2. **Document Retrieval**  
    For each sub-query, we retrieve _m_ relevant documents from the knowledge base.

3. **Re-ranking with RRF**  
    All retrieved documents are re-ranked using the Reciprocal Rank Fusion (RRF) algorithm, which aggregates scores across queries to prioritize the most relevant content.

4. **Fusion and Response Generation**  
    The top fused documents and the set of sub-queries are provided to the LLM, which synthesizes a detailed and factual answer.

---

## 🛠️ Features

- **Multi-query Expansion:** Improves recall by exploring diverse phrasings of the user's question.
- **RRF-based Fusion:** Robustly combines evidence from multiple retrievals ([see paper](https://arxiv.org/pdf/2402.03367)).
- **LLM-powered Synthesis:** Generates comprehensive answers grounded in retrieved evidence.

---

## 📦 Example Pipeline

```python
user_query = "What is Amazon AWS?"
response = Fusion_RAG_Pipeline(user_query)
print(response)
```

---
## CITATION
```bibtex
@article{Rackauckas_2024,
   title={Rag-Fusion: A New Take on Retrieval Augmented Generation},
   volume={13},
   ISSN={2319-4111},
   url={http://dx.doi.org/10.5121/ijnlc.2024.13103},
   DOI={10.5121/ijnlc.2024.13103},
   number={1},
   journal={International Journal on Natural Language Computing},
   publisher={Academy and Industry Research Collaboration Center (AIRCC)},
   author={Rackauckas, Zackary},
   year={2024},
   month=feb, pages={37–47} }

```
---

## 📚 Reference

- **RAG-FUSION: A NEW TAKE ON RETRIEVAL-AUGMENTED GENERATION**  
  [arXiv:2402.03367](https://arxiv.org/pdf/2402.03367)

---

## ✨ Why Use Fusion RAG?

- 🔍 **Better Coverage:** Multiple queries ensure broader information retrieval.
- 🏆 **Improved Ranking:** RRF fusion surfaces the most relevant documents.
- 🤖 **LLM Integration:** Final answers are both accurate and contextually rich.

---

## 🚦 Get Started

1. Prepare your document corpus in the `data/` directory.
2. Run the notebook cells in order.
3. Use `Fusion_RAG_Pipeline(your_query)` to get high-quality, fused responses!

---

Happy experimenting! 💡