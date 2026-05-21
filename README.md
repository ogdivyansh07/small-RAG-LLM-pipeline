# Chat with PDF using Local RAG

![Python](https://img.shields.io/badge/Python-3.11-blue)
![Streamlit](https://img.shields.io/badge/Streamlit-AI_App-red)
![LangChain](https://img.shields.io/badge/LangChain-RAG-green)
![License](https://img.shields.io/badge/License-MIT-yellow)

A privacy-focused Retrieval-Augmented Generation (RAG) application that enables users to interact with PDF documents using natural language queries.

Built with Streamlit, LangChain, Ollama, and DeepSeek-R1, the application processes PDFs locally, retrieves semantically relevant content, and generates concise AI-powered answers — all without external APIs.

---

# Features

- Semantic PDF search using vector embeddings
- Context-aware question answering
- Fully local RAG pipeline
- Streamlit chat interface
- In-memory vector indexing
- Retrieval-based response generation
- Modular LangChain pipeline
- Privacy-friendly offline execution

---

# Screenshots

## Upload Interface
![Upload UI](images/upload-ui.png)

## Chat Interface
![Chat UI](images/chat-ui.png)

## Response Generation
![Response UI](images/response-ui.png)

---

# Demo

![Demo](images/demo.gif)

---

# System Architecture

```text
PDF Upload
    ↓
Text Extraction
    ↓
Chunking
    ↓
Embedding Generation
    ↓
Vector Store
    ↓
Similarity Search
    ↓
LLM Response Generation
```

---

# Tech Stack

| Technology | Purpose |
|------------|----------|
| Python | Core programming |
| Streamlit | Frontend UI |
| LangChain | RAG orchestration |
| Ollama | Local LLM serving |
| DeepSeek-R1 | Response generation |
| PDFPlumber | PDF text extraction |

---

# How RAG Works

1. PDF text is extracted using PDFPlumber.
2. The text is split into overlapping chunks.
3. Embeddings are generated using `nomic-embed-text`.
4. Embeddings are stored inside an in-memory vector database.
5. User queries are converted into embeddings.
6. Similar chunks are retrieved using semantic similarity search.
7. Retrieved context is passed to DeepSeek-R1 through Ollama.
8. The LLM generates a concise contextual answer.

---

# Why Local LLMs?

This project runs entirely offline using Ollama.

## Benefits

- No API costs
- Better privacy
- No internet dependency
- Full local document security
- Faster experimentation with open-source models

---

# Installation

## Clone Repository

```bash
git clone https://github.com/your-username/chat-with-pdf-rag.git
cd chat-with-pdf-rag
```

## Create Virtual Environment

### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

### Linux / Mac

```bash
python -m venv venv
source venv/bin/activate
```

---

# Install Dependencies

```bash
pip install -r requirements.txt
```

---

# Install Ollama

Download and install Ollama from:

https://ollama.com

Pull the required models:

```bash
ollama pull deepseek-r1:8b
ollama pull nomic-embed-text
```

---

# Run the Application

```bash
streamlit run pdf_rag.py
```

---

# Example Queries

- Summarize this PDF
- What are the key findings?
- Explain chapter 2
- What is the conclusion?
- Give me a short overview

---

# Project Structure

```bash
chat-with-pdf/
│
├── pdfs/                 # Uploaded PDFs
├── images/               # README assets
├── pdf_rag.py            # Main Streamlit application
├── test_pdf_rag.py       # Unit tests
├── requirements.txt      # Project dependencies
└── README.md             # Project documentation
```

---

# Future Improvements

- Multi-PDF support
- Persistent vector database (ChromaDB)
- Chat history memory
- Source citation support
- Cloud deployment
- OCR support for scanned PDFs

---

# Contributing

Contributions, issues, and feature requests are welcome.

## Steps

1. Fork the repository
2. Create a new feature branch
3. Commit your changes
4. Push the branch
5. Open a Pull Request

Please ensure:
- Test cases are updated
- Code is properly documented
- PR includes demo screenshots or recordings

---

# Contributors

- Divyansh — Frontend & UI
- Pradhuman — Backend Pipeline
- Kunal — Vector Search & Embeddings
- Pratyush — Testing & Documentation

---

# License

This project is licensed under the MIT License.

---

# Acknowledgments

Special thanks to the teams behind:

- LangChain
- Ollama
- Streamlit
- DeepSeek
- Open-source AI community

for enabling local AI application development.
