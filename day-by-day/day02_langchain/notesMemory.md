# 📘 Day 2 – RAG Chain with Memory (Ollama + LLaMA3)

> **Goal:** Extend the refactored RAG pipeline to support **multi-turn conversational memory** using LangChain's `ConversationalRetrievalChain`.

---

## 🧠 What I Did

- Built on my modular RAG pipeline from earlier
- Introduced **LangChain memory** via `ConversationBufferMemory`
- Switched to `ConversationalRetrievalChain` to handle:
  - Chat history (multi-turn)
  - RAG-based document retrieval
- Used **LLaMA3 via Ollama** to run everything locally
- Debugged LangChain’s strict requirements for memory → fixed by setting both `output_key` values correctly

---

## 🧩 Tech Stack

| Component | Tool |
|----------|------|
| LLM | `ChatOllama(model="llama3")` |
| Memory | `ConversationBufferMemory` |
| Chain | `ConversationalRetrievalChain` |
| Retrieval | `Chroma + HuggingFaceEmbeddings` |
| Docs | `PyPDFLoader` from `langchain_community` |

---

## 🧠 Key Implementation Notes

### ✅ Memory and Chain Setup
```python
memory = ConversationBufferMemory(
    memory_key="chat_history",
    return_messages=True,
    output_key="answer"  # 🛠️ critical to avoid error
)

qa_chain = ConversationalRetrievalChain.from_llm(
    llm=llm,
    retriever=retriever,
    memory=memory,
    return_source_documents=True,
    output_key="answer"  # 🛠️ required for multi-key return
)

while True:
    query = input("🧠 You: ")
    if query.lower() in ["exit", "quit"]:
        break

    result = qa_chain.invoke({"question": query})
    print("🤖", result["answer"])
```
