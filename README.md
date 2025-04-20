# DocuMind-QA-AI-Agent-using-RAG-and-LangChain

## Table of Contents
- [Overview](#overview)
- [Project Aim](#project-aim)
- [Technologies Used](#technologies-used)
- [Prerequisites](#prerequisites)
- [Installation & How to Run](#installation--how-to-run)
- [Usage](#usage)
- [Demo](#demo)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)
- [Contact](#contact)

## Overview
The DocuMind QA AI Agent is the capstone project of the IBM AI Engineering Specialization, showcasing a fully integrated, production-level application. This AI-powered Question Answering (QA) bot is capable of reading PDF documents and answering natural language questions based on their content.

Designed for scenarios like navigating corporate knowledge bases, legal contracts, or technical manuals, the system provides fast and accurate information retrieval. It leverages LangChain to orchestrate a retrieval-augmented generation (RAG) pipeline and integrates the Mixtral 8x7B foundation model hosted on IBM Watsonx.ai for generating human-like answers. The bot turns static PDFs into dynamic, queryable sources of truth.

The entire pipeline is wrapped in an intuitive Gradio interface, ensuring accessibility for both technical and non-technical users.

## Project Aim
The goal of this project was to create a modular and scalable QA system that leverages document intelligence and state-of-the-art large language models.

Key features implemented:
- **Document Loaders**: For parsing PDF content.
- **Text Splitters**: To break down large documents into manageable chunks.
- **Embedding Models**: To semantically encode text.
- **Vector Store (FAISS)**: To enable efficient similarity-based retrieval.
- **Retriever + WatsonxLLM**: To form a powerful RAG pipeline.
- **Gradio Interface**: For interactive question answering.

The system efficiently reads and reasons over large document sets with minimal latency, demonstrating the integration of LangChain, IBM Watsonx.ai, and Hugging Face models in a real-world AI application.

## Technologies Used
- **Programming Language:** Python
- **Libraries:** LangChain, Gradio, Hugging Face Transformers
- **Tools:** IBM Watsonx.ai, FAISS, Jupyter Notebook

## Prerequisites
- Python 3.x
- LangChain
- Gradio
- Hugging Face Transformers
- FAISS

## Installation & How to Run
To set up and run the project locally:

1. **Clone the Repository**:
    ```sh
    git clone https://github.com/ImaadhRenosh/DocuMind-QA-AI-Agent-using-RAG-and-LangChain.git
    cd DocuMind-QA-AI-Agent-using-RAG-and-LangChain
    ```

2. **Install Dependencies**:
    ```sh
    pip install -r requirements.txt
    ```

3. **Run the Application**:
    Launch the Gradio interface:
    ```sh
    python app.py
    ```

## Usage
After running the application:
- Upload PDF documents.
- Ask natural language questions based on the content of the documents.
- Receive accurate, human-like answers.

## Demo
### Main Components:
- **Document Loaders**: Parsing PDF content for downstream processing.
- **Text Splitting**: Breaking down large documents into manageable chunks.
- **Embedding Models**: Encoding document content semantically for efficient retrieval.
- **FAISS Vector Store**: Storing embeddings and enabling similarity search.
- **Gradio UI**: Providing an interactive interface for users.

### Workflow:
1. Upload your PDF document.
2. The system parses the document and splits it into chunks.
3. Chunks are semantically encoded using embedding models.
4. The FAISS vector store retrieves relevant chunks based on user queries.
5. WatsonxLLM generates accurate, natural language answers.

## Contributing
Contributions are welcome! If you’d like to improve this project, please follow these steps:
1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Commit your changes and push the branch.
4. Open a pull request detailing your changes.

## License
This project is licensed under © IBM Corporation. All rights reserved.

## Acknowledgements
- Thanks to the contributors of LangChain, Gradio, Hugging Face Transformers, and FAISS.
- Special thanks to IBM Watsonx.ai for providing the foundation models.

## Contact
For any questions or suggestions, feel free to reach out:
- **Email:** imaadhrenosh@gmail.com
- **LinkedIn profile**: [LinkedIn profile](https://www.linkedin.com/in/imaadh-renosh-007aba348)
