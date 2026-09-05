# 📄 Document Question Answering System

A **Retrieval-Augmented Generation (RAG)** based application that allows users to ask questions about PDF documents and receive answers based on their content.

The application uses **Streamlit** for the interface, **LangChain** for the RAG pipeline, **FAISS** for vector storage, **Google Generative AI** for embeddings, and **Llama 3 8B through Groq** for answer generation.

## 🚀 Features

* 📑 Load PDF documents from the `Artifacts` folder
* ✂️ Split documents into smaller chunks
* 🔢 Generate embeddings using Google Generative AI
* 🔎 Retrieve relevant document content using FAISS
* 🤖 Generate context-based answers using Llama 3
* 🖥️ Interactive Streamlit interface
* ⏱️ Display response time

## 🏗️ How It Works

```text
PDF Documents
      ↓
PDF Loader
      ↓
Text Chunking
      ↓
Google AI Embeddings
      ↓
FAISS Vector Store
      ↓
User Question
      ↓
Document Retrieval
      ↓
Llama 3 + Retrieved Context
      ↓
Final Answer
```

The documents are split using a **chunk size of 1000** with an **overlap of 200** before being converted into embeddings and stored in FAISS.

## 🛠️ Tech Stack

* **Python**
* **Streamlit**
* **LangChain**
* **Groq**
* **Llama 3 8B**
* **Google Generative AI Embeddings**
* **FAISS**
* **PyPDFDirectoryLoader**

## 📂 Project Structure

```text
Question-Answering-System/
│
├── Artifacts/
│   └── *.pdf
│
├── app.py
├── requirements.txt
├── .env
└── README.md
```

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/taranghirapara77-commits/Question-Answering-System.git
cd Question-Answering-System
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Configure API Keys

Create a `.env` file:

```env
API_KEY=your_groq_api_key
GOOGLE_API_KEY=your_google_api_key
```

### 4. Add Documents

Place your PDF files inside the `Artifacts` folder.

### 5. Run the application

```bash
streamlit run app.py
```

## 💡 Usage

1. Add your PDF documents to the `Artifacts` folder.
2. Run the application.
3. Click **"Ingest the Data into Vector Store"**.
4. Enter a question related to your documents.
5. The system retrieves relevant information and generates an answer.

## 🔮 Future Improvements

* Support direct PDF uploads
* Persistent vector database
* Chat history and conversational memory
* Source/page references for answers
* Support for additional document formats
* RAG evaluation and performance metrics

## 👨‍💻 Author

**Tarang Hirapara**

[GitHub](https://github.com/taranghirapara77-commits)
