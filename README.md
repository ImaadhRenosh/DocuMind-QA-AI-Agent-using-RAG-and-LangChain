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
├── app.py                # Main Gradio UI logic
├── qabot.py              # Core QA logic using LangChain, IBM Watsonx
├── requirements.txt      # All necessary Python packages
├── assets/
│   ├── upload_ui.png
│   ├── question_ui.png
│   └── answer_ui.png
└── README.md
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

## 📘 Complete Build & Deployment Guide

I’ve created a comprehensive user manual that walks you through every step — from environment setup to launching the Gradio-powered interface.  

Please follow each step **in order** to ensure smooth execution and deployment.

> ⚠️ **Important:** You must complete all setup steps before accessing the app via the browser. Skipping steps may result in a broken or non-functional link.

> 📖 [Click here to open the Full User Manual](https://github.com/ImaadhRenosh/IBM-Certified-DocuMind-QA-AI-Agent-using-RAG-and-LangChain/blob/main/User%20Manual%20_%20QA%20AI%20Agent%20creation%20guide.pdf)

## 🖥️ Running the App

### ▶️ Run Locally
```bash
python app.py
```
Then open [AI-Powered PDF QA AI-Agent](https://imaadhrenosh-7860.theianext-1-labs-prod-misc-tools-us-east-0.proxy.cognitiveclass.ai/) in your browser.

---

## 🌍 Launch on Hugging Face Spaces (Permanent Hosting)

Deploy your Gradio app to Hugging Face for free with GPU support and a permanent public link:

### 1. Install Hugging Face CLI
```bash
pip install huggingface_hub
```

### 2. Log In to Hugging Face
```bash
huggingface-cli login
```
Paste your access token from: https://huggingface.co/settings/tokens

### 3. Deploy
```bash
gradio deploy
```
Follow the prompts to:
- Name your Space
- Set it as public
- Choose a license (e.g., MIT)

✅ This will automatically upload your app to [https://huggingface.co/spaces](https://huggingface.co/spaces)  
✅ You'll receive a **shareable link** like:

```
https://huggingface.co/spaces/YourUsername/pdf-qa-agent
```

---

## 📸 Screenshots

### 1. Upload PDF  
[[Download a PDF for testing →]](https://github.com/ImaadhRenosh/IBM-Certified-DocuMind-QA-AI-Agent-using-RAG-and-LangChain/blob/main/testPDF_A_Comprehensive_Review_of_Low_Rank_Adaptation_in_Large_Language_Models_for_Efficient_Parameter_Tuning-1.pdf)

### 2. Ask Questions  
<img width="1371" alt="Gradio Interface view" src="https://github.com/user-attachments/assets/6461aefb-98d4-46b7-9ba2-e8a524d9b77d" />

### 3. Receive Answers  
<img width="1370" alt="Question and answer demo" src="https://github.com/user-attachments/assets/f19effcb-a0d4-45ee-b80e-96631fcd6ff0" />

---

## 🤝 How Clients Can Use This

- Deploy as an internal document analysis tool  
- Fine-tune on custom PDFs for company-specific Q&A  
- Embed in websites via iframe or Hugging Face share link  

---

## 🧩 Integrations

- **Cloud Deployment**: Docker-compatible  
- **Multi-user Support**: Add auth layer  
- **Logging**: Extend backend to log Q&A sessions  

---

<img width="681" alt="Screenshot 2025-04-24 at 18 30 37" src="https://github.com/user-attachments/assets/a5aa6611-476e-48f4-a000-dcd61e529dd1" />

