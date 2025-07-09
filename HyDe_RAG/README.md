# HyDe RAG: Hypothetical Document Enhanced Retrieval-Augmented Generation 🚀📄

This project implements **HyDe RAG** (Hypothetical Document Enhanced Retrieval-Augmented Generation), an advanced RAG pipeline that improves retrieval and answer generation by leveraging hypothetical answers. Instead of retrieving context solely based on the user query, HyDe RAG first generates one or more hypothetical answers to the query, embeds them, and uses these embeddings to retrieve the most relevant document chunks. This approach can improve retrieval quality, especially for complex or ambiguous queries.

Inspired from the research paper of HyDe : [Precise Zero-Shot Dense Retrieval without Relevance Labels](https://arxiv.org/pdf/2212.10496)
---

## Features ✨

- **Single and Multiple HyDe Modes:**  
    Generate one or several hypothetical answers for a query, and use their embeddings (averaged in the multi-hypo case) for retrieval. 🤔➡️📚
- **Flexible LLM and Embedding Integration:**  
    Uses Google Gemini for LLM and Google GenAI for embeddings. 🤖🔗
- **Semantic Scoring:**  
    Retrieved chunks are scored for semantic similarity to the hypothetical answer(s). 🧠📈
- **Chunked Document Processing:**  
    Documents are split into manageable chunks for efficient retrieval and ranking. ✂️📄
- **Easy-to-Use Functions:**  
    Includes `HydeRAG` and `HydeRAG_Multiple` for single and multi-hypothetical workflows. 🛠️

---

## Workflow 🔄

1. **Document Loading & Chunking:**  
     Documents are loaded from the `data` directory and split into chunks using `SentenceSplitter`. 📂✂️

2. **Embedding & LLM Setup:**  
     Google GenAI embeddings and Gemini LLM are configured. 🧩🤖

3. **Indexing:**  
     Chunks are indexed using a vector store for fast similarity search. 🗂️⚡

4. **Hypothetical Answer Generation:**  
     For a given query, the LLM generates one or more plausible answers (hypotheticals). 💡

5. **Embedding Hypotheticals:**  
     Each hypothetical answer is embedded. In multi-hypo mode, embeddings are averaged. 🧬➗

6. **Retrieval:**  
     The hypothetical embedding(s) are used to retrieve the most relevant document chunks. 🎯

7. **Scoring & Ranking:**  
     Retrieved chunks are scored (cosine similarity or semantic evaluator) and ranked. 🏅

8. **Final Answer Generation:**  
     The top-ranked chunks are provided as context to the LLM to generate the final answer. 📝

---

## 📖 References

- [HyDe RAG Paper (arXiv:2212.10496)](https://arxiv.org/pdf/2212.10496)

---
# Custom Chunk Retrieval Implementation 🛠️

Unlike out-of-the-box retrieval solutions, this project implements chunk retrieval from scratch for maximum flexibility and transparency:

- **Document Chunking:** Documents are split into manageable chunks using a sentence-based splitter.
- **Embedding:** Both queries (or their hypothetical answers) and document chunks are embedded using Google GenAI.
- **Similarity Scoring:** Retrieved chunks are scored using either cosine similarity or semantic evaluators, allowing for fine-grained ranking.
- **Manual Ranking:** The code sorts and selects the top-k chunks based on similarity scores, ensuring only the most relevant context is used for answer generation.

This custom approach allows for experimentation with different retrieval strategies, scoring methods, and chunking techniques, making the system highly adaptable and research-friendly.

---

Feel free to refer to the code cells for detailed implementation of each step!