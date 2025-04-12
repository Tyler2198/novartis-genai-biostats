# 📘 Day 1 – RAG Systems 101

> **Goal:** Understand and implement a working prototype of Retrieval-Augmented Generation (RAG) using LangChain, ChromaDB, and Hugging Face embeddings.

---

## 🧠 What is RAG?

**RAG (Retrieval-Augmented Generation)** is a method that enhances the capabilities of LLMs by allowing them to retrieve external knowledge from a document store to generate grounded, factual answers.

### ⚙️ RAG Pipeline Components:
1. **Document Ingestion** – Load structured/unstructured data (e.g., PDFs).
2. **Text Chunking** – Split documents into digestible pieces (chunks).
3. **Embeddings** – Convert text chunks into vector representations.
4. **Vector Store** – Store and retrieve chunks based on semantic similarity.
5. **Retriever + Prompt + LLM** – Compose a chain to:
   - Retrieve relevant chunks
   - Format a prompt with context
   - Generate an accurate answer

---

## 🛠️ Tools & Libraries Used

| Tool | Purpose |
|------|---------|
| **LangChain** | Build modular LLM chains |
| **ChromaDB** | Fast and local vector database |
| **Hugging Face Embeddings** | Generate dense vector representations |
| **PyPDFLoader** | Parse content from PDF documents |
| **PromptTemplate** | Define input structure for LLMs |
| **RunnablePassthrough / OutputParser** | Control flow and parse LLM output |

---

## 📄 Document Used

We loaded a real-world medical document (PDF) that could represent internal Novartis materials like:
- **GMA Strategy Documents**
- **Neato Internal Guides**
- **Scientific Literature**

---

## 💡 Highlights from the Implementation

### ✅ Loading and Chunking
```python
loader = PyPDFLoader("TS3043166.pdf")
docs = loader.load()

text_splitter = RecursiveCharacterTextSplitter(chunk_size=1000, chunk_overlap=200)
splits = text_splitter.split_documents(docs)
