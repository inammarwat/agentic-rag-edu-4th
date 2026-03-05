# Agentic-RAG-Edu: Intelligent Student Support System for KazNU

[![Python 3.13](https://img.shields.io/badge/python-3.13-blue.svg)](https://www.python.org/downloads/)
[![LangChain](https://img.shields.io/badge/Framework-LangChain_v1.0-green.svg)](https://python.langchain.com/)
[![LLM](https://img.shields.io/badge/LLM-Gemini_2.5_Flash-orange.svg)](https://deepmind.google/technologies/gemini/)

## 📌 Project Overview
**Agentic-RAG-Edu** is an advanced AI-driven Student Support System designed for Al-Farabi Kazakh National University (KazNU). This project transitions from a standard **Retrieval-Augmented Generation (RAG)** pipeline to an **Agentic Framework**, allowing the system to reason, use external tools, and provide grounded answers based on official university documentation.

This project serves as the core practical component of my Master's Dissertation in Data Science at KazNU.

## 🏗️ System Architecture
The system evolved through three distinct phases:
1.  **Semantic Search Baseline:** Using local embeddings for document retrieval.
2.  **Simple RAG (LCEL):** A structured pipeline connecting retrieval to Google Gemini.
3.  **Agentic RAG (ReAct):** A reasoning loop that utilizes tools (PDF Search + Web Search) to solve complex, multi-step student queries.



## 🛠️ Tech Stack
* **LLM:** Google Gemini 2.5 Flash (via `langchain-google-genai`)
* **Orchestration:** LangChain (LCEL) & LangGraph
* **Vector Database:** ChromaDB (Persistent local storage)
* **Embeddings:** HuggingFace `all-MiniLM-L6-v2` (Running locally on CPU)
* **Tools:** DuckDuckGo Search API, PyPDF for document parsing
* **Environment:** Python 3.13, UV (Fast package manager)

## 📂 Project Structure
```text
├── .env                  # API Credentials (Hidden)
├── .gitignore            # Version control exclusions
├── pyproject.toml        # Dependency management
├── db/                   # Persistent ChromaDB storage
├── data/                 # Raw PDF Documents (Policies, Booklets)
├── notebooks/
│   ├── 01_Data_Prep.ipynb       # PDF ingestion and chunking
│   ├── 02_Vector_Store.ipynb    # Embedding and DB creation
│   ├── 03_Simple_RAG.ipynb      # Baseline LCEL RAG pipeline
│   └── 04_Agentic_RAG.ipynb     # Reasoning Agent with Tool use
└── README.md


## 🤝 Author
**Engr. Inam Ullah Khan** Master's Student in Data Science | Al-Farabi Kazakh National University

Specialization: NLP & Agentic Systems