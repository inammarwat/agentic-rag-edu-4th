# Agentic-RAG-Edu: Intelligent Student Support System for KazNU

[![Python 3.13](https://img.shields.io/badge/python-3.13-blue.svg)](https://www.python.org/downloads/)
[![LangChain](https://img.shields.io/badge/Framework-LangChain_v1.0-green.svg)](https://python.langchain.com/)
[![LLM](https://img.shields.io/badge/LLM-Gemini_2.5_Flash-orange.svg)](https://deepmind.google/technologies/gemini/)


## Overview

This project presents a **Retrieval-Augmented Generation (RAG) based AI assistant** designed to support students of Al-Farabi Kazakh National University (KazNU) by providing accurate information extracted from official university documents.

The system retrieves relevant information from university policy documents and generates contextual answers using a Large Language Model (LLM). The goal is to assist students in quickly accessing institutional information related to academic policies, procedures, and services.

This work represents the **prototype implementation phase** of the MSc dissertation titled:

**"Design and Development of an Agentic Retrieval-Augmented Generation System for University Information Assistance."**

---

## Key Features

* Document-based question answering system
* Vector search using semantic embeddings
* Retrieval-Augmented Generation (RAG) architecture
* Integration with Google Gemini LLM
* Local vector database using Chroma
* HuggingFace embedding models
* Context-aware response generation

---

## System Architecture

The system follows the **Retrieval-Augmented Generation (RAG)** architecture:

1. University PDF documents are processed and chunked
2. Text embeddings are generated using a sentence-transformer model
3. Embeddings are stored in a **Chroma vector database**
4. When a user asks a question:

   * The retriever finds relevant document chunks
   * Retrieved context is injected into a prompt
   * Gemini LLM generates the final answer

Pipeline:

User Question
→ Retriever (Vector Search)
→ Relevant Document Chunks
→ Prompt Template
→ Gemini LLM
→ Generated Answer

---

## Technologies Used

| Component            | Technology                        |
| -------------------- | --------------------------------- |
| Programming Language | Python                            |
| LLM                  | Google Gemini 2.5 Flash           |
| Embeddings           | HuggingFace Sentence Transformers |
| Vector Database      | Chroma DB                         |
| Framework            | LangChain                         |
| Document Processing  | Python PDF loaders                |
| Environment          | Jupyter Notebook / Python         |


## 🛠️ Tech Stack
* **LLM:** Google Gemini 2.5 Flash (via `langchain-google-genai`)
* **Orchestration:** LangChain (LCEL) & LangGraph
* **Vector Database:** ChromaDB (Persistent local storage)
* **Embeddings:** HuggingFace `all-MiniLM-L6-v2` (Running locally on CPU)
* **Tools:** DuckDuckGo Search API, PyPDF for document parsing
* **Environment:** Python 3.13, UV (Fast package manager)
---

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
```

---

## Example Query

**Student Question**

```
What are the requirements for participating in academic mobility?
```

**System Response**

```
Students can participate in academic mobility within the framework of inter-university agreements or international programs. For internal mobility, a tripartite agreement between the student, sending university, and receiving university is required. For international mobility, an official invitation from the host institution is necessary.
```


---

## Running the System

Run the main RAG script:

```
python rag_pipeline.py
```

Then ask questions related to university policies.

---


## Future Work (Dissertation Phase)

The next phase of this research will implement an **Agentic RAG architecture**, including:

* Multi-agent reasoning
* Query planning agents
* Document verification agents
* Autonomous retrieval strategies
* Evaluation of response accuracy

---

## Author

**Inam Ullah Khan**
Master’s Student – Data Science
Al-Farabi Kazakh National University
Kazakhstan

Research Area:

* Generative AI
* Retrieval-Augmented Generation
* Agentic AI Systems

---

## Repository

GitHub Repository:

https://github.com/inammarwat/agentic-rag-edu-4th
