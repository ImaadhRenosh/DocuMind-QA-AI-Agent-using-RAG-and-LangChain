# AI-Powered PDF QA Bot with IBM Watsonx, LangChain & Gradio

This repository showcases a production-ready, interactive QA bot that allows users to upload PDF files and ask questions about their content. It's powered by IBM Watsonx foundation models, LangChain, and served through a sleek Gradio interface.

---

## 🔧 Features

- 📄 Upload and parse any PDF document
- 🤖 Ask contextual questions and get instant answers
- ⚡ Powered by IBM Watsonx LLM & Embeddings
- 🧠 Uses ChromaDB for efficient vector storage
- 🌐 Clean, user-friendly web interface via Gradio

---

## 📁 Directory Structure
```
├── qabot.py
├── assets/
│   ├── upload_ui.png
│   ├── question_ui.png
│   └── answer_ui.png
├── README.md
└── requirements.txt
```

---

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/pdf-qa-bot.git
cd pdf-qa-bot
```

### 2. Set Up a Virtual Environment
```bash
pip install virtualenv
virtualenv my_env
source my_env/bin/activate
```

### 3. Install Dependencies
```bash
python3.11 -m pip install \
  gradio==4.44.0 \
  ibm-watsonx-ai==1.1.2 \
  langchain==0.2.11 \
  langchain-community==0.2.10 \
  langchain-ibm==0.1.11 \
  chromadb==0.4.24 \
  pypdf==4.3.1 \
  pydantic==2.9.1
```

---

## 🧠 About the Application Logic

### 1. PDF Parsing
Using `PyPDFLoader` from LangChain Community, the PDFs are loaded and split into chunks of 1000 characters using `RecursiveCharacterTextSplitter`.

### 2. Embedding + Vector Store
Chunks are embedded using `WatsonxEmbeddings` (Slate 125M model) and stored in `ChromaDB` for fast retrieval.

### 3. Retrieval-Based QA
We use LangChain’s `RetrievalQA` chain that combines the retriever with `WatsonxLLM` (Mixtral 8x7B) for inference.

---

## 🖥️ Running the App

### Run the bot
```bash
python qabot.py
```
Then open `http://127.0.0.1:7860` in your browser.

---

## 📸 Screenshots

### 1. Upload PDF
![Upload PDF](assets/upload_ui.png)

### 2. Ask Questions
![Question UI](assets/question_ui.png)

### 3. Receive Answers
![Answer UI](assets/answer_ui.png)

---

## 🤝 How Clients Can Use This
- Can be deployed as a private/internal document analysis tool
- Fine-tune on custom PDFs for personalized Q&A
- Embed into websites with iframe or Gradio share link

---

## 🧩 Integrations
- **Cloud Deployment**: Can be containerized with Docker
- **Multi-user Support**: Extend with user authentication
- **Logging**: Add backend logging for questions/answers

---

## 🧠 About Me
Hi, I'm Mohammed Imaadh Renosh — an aspiring AI/ML engineer who’s passionate about real-world applications of LLMs. This project reflects my commitment to building production-grade, client-ready AI solutions. Feel free to reach out or collaborate!

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)](https://www.linkedin.com/in/imaadhrenosh)

---

## 📄 License
MIT License
