# 🚀 Multi-Document Agentic RAG Project 📄🤖

## Overview 📝

This project implements an advanced Retrieval-Augmented Generation (RAG) system that intelligently routes user queries to the most relevant document collections and tools using an agentic approach. Unlike traditional multi-document RAG pipelines that simply combine all documents into a single index, this solution creates separate vector indices for each document or document category (e.g., AWS Overview, Amazon EC2, AWS Lambda, Amazon Business FAQ, Amazon Serverless). An AI agent orchestrates the workflow, leveraging classification, question decomposition, and retrieval tools to provide accurate and context-aware answers.

## Key Features ✨

- **Document Segmentation & Indexing:** 📚  
    Each document or document category is chunked and indexed separately, allowing for targeted retrieval and minimizing irrelevant context.

- **Agentic Orchestration:** 🧠🤖  
    An AI agent coordinates the workflow, deciding when to classify queries, break down complex questions, select the appropriate RAG engine, or fall back to web search.

- **Intelligent Query Routing:** 🗂️➡️  
    The agent uses a classification tool to determine which document index is most relevant for a given query, ensuring precise and efficient retrieval.

- **Compound Question Handling:** 🧩  
    Multi-part or complex queries are automatically split into sub-questions, each routed independently for retrieval and then synthesized into a final answer.

- **Tool Integration:** 🛠️  
    The agent has access to multiple tools, including:
    - RAG engines for each document category
    - Query classification
    - Question decomposition
    - Web search as a fallback or enrichment

- **Modular & Extensible:** 🧱🔌  
    New document categories or tools can be added easily without disrupting the overall workflow.

## Why This Project Stands Out 🌟

- **Fine-Grained Control:** 🎯  
    By maintaining separate indices and using intelligent routing, the system avoids the noise and inefficiency of monolithic multi-doc RAG setups.

- **Agentic Reasoning:** 🧠💡  
    The agent's ability to reason step-by-step, decompose questions, and select the best tool for each sub-task leads to more accurate and contextually relevant answers.

- **Scalability & Maintainability:** 📈🔧  
    The modular design allows for easy scaling to more document types or tools, and simplifies maintenance and updates.

- **Enhanced User Experience:** 😊👍  
    Users receive concise, well-synthesized answers even for complex, multi-faceted queries, thanks to the agent's orchestration.

## How It Works ⚙️

1. **User submits a query.** 💬
2. **Agent determines if the query is compound.** 🕵️‍♂️  
     - If so, it splits the query into sub-questions.
3. **Each (sub-)question is classified** to identify the relevant document category. 🏷️
4. **The appropriate RAG engine is invoked** to retrieve answers from the targeted index. 🤖
5. **If needed, web search is used** to supplement or enrich the answer. 🌐
6. **The agent synthesizes the results** and returns a clear, final answer. 📝✅

---

This approach delivers a robust, intelligent, and extensible RAG system that goes beyond simple multi-document retrieval, offering agentic reasoning and precise information routing for superior results. 🏆