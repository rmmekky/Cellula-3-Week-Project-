# Cellula-3-Week-Project-
# 🧩 RAG Code Generation System using HumanEval Dataset

This project implements a **Retriever-Augmented Generation (RAG)** pipeline designed specifically for **code generation**.  
The system takes a natural language programming task (e.g., “Write a function that reverses a list”) and:

1. Retrieves **similar coding examples** from the **HumanEval** dataset.
2. Uses an **open-source LLM** (HuggingFace or OpenRouter model) to generate high-quality Python code.
3. Produces a final function with contextual awareness of previously solved tasks.

---

# 📌 Features

- Load and preprocess the **HumanEval dataset**  
- Extract the following fields:  
  - `task_id`  
  - `prompt` (task description)  
  - `canonical_solution`  
- Build embedding pipeline using:
  - **Falcon**, **SentenceTransformers**, or any open-source embedding model
- Store embeddings using **FAISS** or **ChromaDB**
- Retrieve top-k similar examples for any new query
- Generate Python code using:
  - CodeLLaMA, StarCoder, Qwen-Code, or any open-source code LLM
- Fully modular design:
  - `dataset_loader.py`
  - `embedder.py`
  - `vectorstore.py`
  - `retriever.py`
  - `generator.py`
  - `pipeline.py` (end-to-end RAG)

---

# 📁 Project Structure

