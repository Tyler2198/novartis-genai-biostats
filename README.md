# 🧬 Novartis GenAI Biostatistics Internship – Full Preparation Plan

Welcome to my preparation repository for the **Generative AI Biostatistics Internship** at **Novartis Basel**, starting **May 1st, 2025**.

This internship focuses on developing **Generative AI Proof-of-Concepts** (POCs) in:
- 🤖 Retrieval-Augmented Generation (RAG) systems
- 🧾 Automated generation of TFLs (Tables, Figures, Listings) in R
- 🧠 Integration of LLMs into medical affairs workflows

This repo documents my full 3-week structured preparation program, including daily tasks, notes, code experiments, and mini-projects.

---

## 🗓️ 3-Week Master Plan

| Week | Theme             | Focus Area                                                                 |
|------|-------------------|----------------------------------------------------------------------------|
| 1️⃣ Week 1 | Core Concepts       | Learn RAG architecture, embeddings, LangChain, prompt engineering, R basics |
| 2️⃣ Week 2 | Hands-on Projects   | Build RAG chatbots and auto-code TFL generators                         |
| 3️⃣ Week 3 | Simulations & Demos | Simulate real Novartis workflows and polish codebase                    |

---

## 🔧 Week 1: Foundations

> Deep dive into Retrieval-Augmented Generation, LangChain, prompt engineering, and R for medical reporting.

| Day | Focus                        | Deliverable                                           |
|-----|-----------------------------|--------------------------------------------------------|
| 1   | RAG Systems 101             | First full RAG chatbot prototype                      |
| 2   | LangChain Deep Dive         | Custom chains, retrievers, memory                     |
| 3   | Prompt Engineering          | Best practices for QA, summarization, and code tasks  |
| 4   | Parsing Medical Docs        | Load and preprocess PDFs, DOCX, structured tables     |
| 5   | Intro to R for TFLs         | Practice with `gtsummary`, `gt`, `flextable`          |
| 6   | LLM Code Generation         | Use GPT to generate & validate R code templates       |
| 7   | Wrap-Up: Mini LangChain Agent | Chatbot + code generation combo experiment          |

---

## 🛠️ Week 2: Projects & Prototypes

> Apply what you’ve learned to realistic use cases with simulated data.

| Day | Focus                        | Deliverable                                           |
|-----|-----------------------------|--------------------------------------------------------|
| 8   | Project 1: GMA RAG Bot      | Chatbot built on GMA doc PDF                          |
| 9   | Project 2: Neato QA Chain   | Multi-doc QA on simulated Novartis tools              |
| 10  | Project 3: TFL Generator    | R code auto-generation from metadata specs            |
| 11  | Evaluation Metrics          | Retrieval & response validation, QA accuracy          |
| 12  | Code + Chat Integration     | Code generation via chatbot UX                        |
| 13  | TFL Testing Automation      | Unit tests for correctness and visual layout          |
| 14  | Project Documentation       | Markdown summary with visuals + GitHub cleanup        |

---

## 🚀 Week 3: Simulate Internship Workflows

> Simulate your day-to-day internship tasks and polish delivery-ready assets.

| Day | Focus                        | Deliverable                                           |
|-----|-----------------------------|--------------------------------------------------------|
| 15  | GMA Chatbot (Final Version) | Fully integrated RAG chatbot                          |
| 16  | Metadata-to-TFL Pipeline    | Convert layouts to final table outputs                |
| 17  | System Testing              | Robustness, performance, edge case handling           |
| 18  | Final Repo Polish           | README, notebooks, notes, diagrams                    |
| 19  | Dry Run Day (May 1 Sim)     | Demo presentation + walkthrough script                |
| 20  | Buffer/Optional Topics      | Reinforcement learning, LangGraph, agents             |
| 21  | Ready to Fly ✈️              | Final review, commit everything, relax                |

---

## 📁 Repository Structure

novartis-genai-biostats-internship/ ├── day-by-day/ # Daily tasks, notes, experiments │ ├── day01_rag_basics/ │ ├── day02_langchain/ │ ├── ... ├── rag_projects/ # Custom RAG chatbots (GMA, Neato) ├── tfl_genai/ # R code generation templates │ ├── r_templates/ │ └── metadata_examples/ ├── notebooks/ # Scratch notebooks and testing ├── resources/ # Research papers, links, reading material ├── README.md # This file └── .gitignore

---

## 🧠 Tools & Technologies

| Category       | Stack                                                                 |
|----------------|----------------------------------------------------------------------|
| LLMs           | OpenAI GPT-4, Claude, Hugging Face Transformers                      |
| Retrieval      | ChromaDB, FAISS, LangChain, LlamaIndex                               |
| Embeddings     | `all-MiniLM-L6-v2`, OpenAI Embeddings                                |
| R TFL Libraries| `gtsummary`, `gt`, `flextable`, `dplyr`, `janitor`                   |
| LangChain      | Chains, Retrievers, Agents, Output Parsers, Memory, PromptTemplates |
| Workflow       | Python, Jupyter, Markdown, GitHub                                    |

---

## 📌 Why This Matters

Novartis' Medical Affairs and RWE teams rely heavily on documentation, structured reporting, and validated code outputs.  
This preparation ensures I can:

- ✅ Build production-ready RAG systems for internal use
- ✅ Automatically generate validated, consistent R code for medical reports
- ✅ Communicate, document, and demo GenAI pipelines clearly

---

## ✨ Final Goal

> Arrive on **Day 1 at Novartis** with a working knowledge of:
> - RAG pipelines
> - LLM integration into internal tools
> - Template-based code generation in R
> - Industry-grade GitHub documentation

---

Let’s build something that matters. 💊🧬
