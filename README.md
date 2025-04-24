# AI-Powered PDF QA AI-Agent with IBM Watsonx, LangChain & Gradio

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
Then open [AI-Powered PDF QA AI-Agent](https://imaadhrenosh-7860.theianext-1-labs-prod-misc-tools-us-east-0.proxy.cognitiveclass.ai/) in your browser.

---

## 📸 Screenshots

### 1. Upload PDF
[![upload pdf](path/to/your/image.png)](https://github.com/ImaadhRenosh/IBM-Certified-DocuMind-QA-AI-Agent-using-RAG-and-LangChain/blob/main/testPDF_A_Comprehensive_Review_of_Low_Rank_Adaptation_in_Large_Language_Models_for_Efficient_Parameter_Tuning-1.pdf)

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


