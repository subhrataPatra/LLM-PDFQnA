# 🧠 PDF Question-Answering Bot with LangChain & ChromaDB

This project demonstrates a simple **PDF-based Q&A chatbot** using Retrieval-Augmented Generation (RAG) architecture. It loads a PDF, processes the content, stores vector embeddings, and answers user questions using a lightweight LLM model.

---

## 🔧 Tech Stack
- **LangChain**
- **Hugging Face Embeddings** (no token needed)
- **Chroma DB** (Vector Store)
- **PyPDFLoader**
- **SentenceTransformers**
- **PDF Input: 53-page Human Rights document**

---

## 📋 Features
- ✅ Loads and splits PDFs into text chunks
- ✅ Generates sentence-level embeddings
- ✅ Stores embeddings in Chroma vector DB
- ✅ Retrieves relevant chunks for user questions
- ✅ Uses basic LLM model to generate responses

---

**PDF → Pages → Chunks → Embeddings → Chroma
                               ⬇
                     Retriever (search by similarity)
                               ⬇
        Question + Top Chunks → LLM → Final Answer**


## 📉 Current Output Quality (Known Issues)
- Some answers are **repetitive** or **too generic**
- Caused by small model size and lack of tuned prompt
- Output: `"the document is about human rights related to human rights..."`

This version is a **first milestone** and will be improved with better models and prompts.

---

## 🔄 Planned Improvements
- Upgrade to better model (Zephyr, Mistral, or GPT-4 via API)
- Apply prompt engineering for concise, relevant answers
- Add document citation in output
- Build a Streamlit UI
- Evaluate output quality via retrieval metrics (EM/F1/ROUGE)

---

## 📁 Example
```bash
Input Question: What is the document about?
Output: the document is about human rights related to human rights...
```markdown
## 🐍 Python Version

This project was tested using:

```bash
Python 3.10
