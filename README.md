


# 📘 PDF-Based Question Answering System (RAG Pipeline)

This project is a lightweight Retrieval-Augmented Generation (RAG) pipeline that lets you upload a **PDF of notes**, extract text, embed it, search relevant content with **FAISS**, and generate **exam-ready answers** using the **Falcon-7B-Instruct** LLM.

---

## 🚀 Features

* 📄 **PDF Extraction** using PyMuPDF
* ✂️ **Automatic sentence chunking** with regex
* 🧠 **Semantic Embeddings** via Sentence-Transformers
* ⚡ **FAISS vector search** for fast context retrieval
* 🤖 **Falcon-7B-Instruct** for clean, detailed answer generation
* 🗂️ Multi-question support
* 🔍 Designed for study, assignments, and exam prep

---

## 🧩 How It Works

1. Upload your PDF notes.
2. The script extracts and splits text into sentences.
3. Embeddings are generated for every sentence.
4. FAISS finds the most relevant chunks for each question.
5. Falcon-7B-Instruct generates a final polished answer using retrieved context.

---

## 📦 Requirements

```txt
PyMuPDF (fitz)
numpy
faiss-cpu
torch
sentence-transformers
transformers
google-colab (if running on Colab)
```

Install:

```bash
pip install pymupdf numpy faiss-cpu torch sentence-transformers transformers
```

---

## ▶️ Usage

1. Run the script in Google Colab or locally with GPU.
2. Upload your notes PDF when prompted.
3. Enter your questions (one per line).
4. The system retrieves relevant content and generates answers automatically.

---

## 📜 Code Overview

* `extract_text_from_pdf()` – Reads the full PDF
* `split_into_sentences()` – Splits long text into manageable chunks
* `create_embeddings()` – Converts text → vector embeddings
* `build_faiss_index()` – Builds and stores vectors in FAISS
* `get_contexts()` – Retrieves top-k relevant sentences
* Falcon-7B uses these to produce clean, exam-style answers

---

## 💡 Example Output

```
Question: What is reinforcement learning?
Answer:
Reinforcement Learning is a machine learning approach where...
```

---

## 🧑‍💻 Author Skills Highlight

Built end-to-end RAG system integrating **Python**, **NLP**, **vector search**, **LLM orchestration**, and **document processing pipelines**.


