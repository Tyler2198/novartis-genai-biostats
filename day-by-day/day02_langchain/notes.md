# 📘 Day 2 – Refactored RAG Chain (Ollama + LLaMA3)

> **Goal:** Refactor my Day 1 RAG prototype into clean, modular code with reusable functions, replacing OpenAI with a local LLaMA3 model via Ollama.

---

## 🧠 What I Did

- Extracted my notebook logic into a standalone Python script (`basic_rag_chain_refactored.py`)
- Wrapped PDF parsing, chunking, embedding, retrieval, and chaining into clean functions
- Replaced `ChatOpenAI` with `ChatOllama` and used the **LLaMA3** model locally
- Verified the chain's behavior using a custom query
- Set up the code to be **scalable** and **production-ready**

---

## ⚙️ Components Overview

| Component | Description |
|----------|-------------|
| `load_documents()` | Loads a medical PDF using `PyPDFLoader` |
| `split_documents()` | Splits the content into overlapping chunks for better retrieval |
| `create_vectorstore()` | Embeds chunks using HuggingFace model and stores them in a Chroma DB |
| `build_rag_chain()` | Composes a pipeline using retriever → prompt → LLaMA3 LLM → output parser |
| `main()` | Loads everything and executes the query chain |

---

## 🔁 The Chain

Implemented using **LangChain Expression Language**, the pipeline was built like this:

```python
rag_chain = (
    {
        "context": retriever | format_docs,
        "question": RunnablePassthrough()
    }
    | prompt
    | llm
    | StrOutputParser()
)
