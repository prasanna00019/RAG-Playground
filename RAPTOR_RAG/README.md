# 🌳 RAPTOR RAG: Recursive Abstractive Processing for Tree-Organized Retrieval 🌲

Welcome to the RAPTOR RAG project! This repository contains a from-scratch implementation of the RAPTOR (Recursive Abstractive Processing for Tree-Organized Retrieval) approach, inspired by the research paper [RAPTOR: RECURSIVE ABSTRACTIVE PROCESSING FOR TREE-ORGANIZED RETRIEVAL](https://arxiv.org/pdf/2401.18059v1) .

---

## 📚 Overview

RAPTOR is a novel retrieval-augmented generation (RAG) framework that organizes document chunks into a hierarchical tree using recursive clustering and abstractive summarization. This structure enables efficient and context-rich retrieval for downstream question answering and information retrieval tasks.

---

## 🚀 Features

- **Recursive Tree Construction:** Documents are recursively clustered (using Gaussian Mixture Models) and summarized to build a multi-level tree.
- **Abstractive Summarization:** Each cluster is summarized using an LLM, capturing the essence of grouped texts.
- **Flexible Querying:** Supports both:
    - **Tree Traversal Method:** Traverses the tree top-down, selecting relevant nodes at each level.
    - **Tree Collapse Method:** Collapses the tree into a flat set and retrieves the most relevant nodes up to a token limit.
- **Visualization:** Includes GMM clustering visualization for synthetic embeddings.
- **Modular & Extensible:** Easily swap out embedding models, LLMs, and clustering strategies.

---

## 🛠️ How It Works

1. **Document Loading:** Documents are loaded and split into manageable chunks.(also used semantic chunking)
2. **Embedding & Clustering:** Chunks are embedded and clustered recursively using GMM.
3. **Summarization:** Each cluster is summarized via an LLM, forming parent nodes in the tree.
4. **Tree Construction:** The process repeats until the tree root is reached.
5. **Querying:** Retrieve relevant context using either tree traversal or tree collapse methods.
6. **Answer Generation:** The retrieved context is used to generate answers to user queries.

---

## 📊 Example: GMM Clustering Visualization

The notebook includes a demonstration of GMM clustering on synthetic 5D embeddings, visualized in 2D using PCA, to illustrate the clustering process used in RAPTOR.

---

## 📦 Usage

- Clone the repository and install the required dependencies.
- Follow the notebook cells to load your data, build the RAPTOR tree, and perform queries.
- Switch between tree traversal and tree collapse querying as needed.

---

## 📄 Reference

This implementation is inspired by:

> RAPTOR: RECURSIVE ABSTRACTIVE PROCESSING FOR TREE-ORGANIZED RETRIEVAL. [arXiv:2401.18059v1](https://arxiv.org/pdf/2401.18059v1)

---

## 💡 Acknowledgements

- Thanks to the RAPTOR authors for their innovative work!
- Built with 🤗 [LlamaIndex](https://github.com/jerryjliu/llama_index), [LangChain](https://github.com/langchain-ai/langchain), and [scikit-learn](https://scikit-learn.org/).

---

## 📝 Explore the Code

Check out the notebook cells below for detailed implementation, usage examples, and visualizations!

---

Happy experimenting! 🚀