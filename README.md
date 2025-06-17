# PDF-RAG-Chatbot-AI-Powered-Document-Q-A-with-LangChain

This project is a **Retrieval-Augmented Generation (RAG)** based chatbot that allows users to upload a PDF document and ask questions based on its content. Built using **IBM Foundation Models**, **LangChain**, and **Gradio**, the application intelligently retrieves and generates context-aware answers from the uploaded document.

---

## 🚀 Features

- 🔍 Retrieval-based QA using PDF documents
- 🧠 Powered by open-access Foundation Models
- 📑 PDF parsing & chunking with `PyPDFLoader` and `RecursiveCharacterTextSplitter`
- 🔗 Embedding and Vector DB with Chroma and custom embedding models
- 🧱 LangChain RetrievalQA for document-grounded response generation
- 🌐 Interactive user interface with Gradio

---

## 🧰 Tech Stack

- **LLM**: `mixtral-8x7b-instruct-v01` via IBM Foundation Model API
- **Embedding Model**: `slate-125m-english-rtrvr`
- **Libraries**: LangChain, Gradio, ChromaDB
- **Document Format Supported**: `.pdf`

---

## 🧑‍💻 How It Works

1. **User Uploads a PDF**
2. **PDF is parsed** using `PyPDFLoader`
3. **Text is split** into chunks with overlaps
4. **Embeddings are created**
5. **Chroma Vector Store** indexes the chunks
6. **Retriever pulls** relevant text chunks
7. **LLM generates** the answer from retrieved chunks

---

## 📦 Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/pdf-rag-chatbot.git
cd pdf-rag-chatbot

python3.11 -m venv my_env
source my_env/bin/activate  # For Windows: my_env\Scripts\activate
python3.11 -m pip install \
  gradio==4.44.0 \
  ibm-watsonx-ai==1.1.2  \
  langchain==0.2.11 \
  langchain-community==0.2.10 \
  langchain-ibm==0.1.11 \
  chromadb==0.4.24 \
  pypdf==4.3.1 \
  pydantic==2.9.1

