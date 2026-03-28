# ai-engineering-workbench
A repository dedicated to exploring the implementation of Generative AI, focusing on moving models into production-ready environments.

## 🗺️ Project Roadmap

- **[01_core_concepts](./01_core_concepts/):** Benchmarking and safety guardrails.
- **[02_embeddings_lab](./02_embeddings_lab/):** Deep dive into semantic similarity.
- **[03_vector_databases](./03_vector_databases/):** Persistent memory with ChromaDB.
- **[04_rag_pipelines](./04_rag_pipelines/):** Building context-aware systems.
- **[05_agentic_workflows](./05_agentic_workflows/):** The shift to Autonomous Systems (ReAct & Function Calling).
- **[06_prototypes](./06_prototypes/):** Full-stack AI applications like **NexusNote**.


## 1.Prototype

# 📂 NexusNote: Chat with Your Docs

**NexusNote** is a high-speed RAG (Retrieval-Augmented Generation) application built to transform static text documents into an interactive knowledge base. No more manual searching through long PDFs or text files—just ask NexusNote.

## 🚀 The Build
This project was developed as part of a deep-dive into AI Engineering. The goal was to move beyond simple API calls and build a resilient, production-ready system that handles real-world deployment challenges.

### 🛠️ Tech Stack
* **LLM Engine:** Llama 3.3-70B (via **Groq LPU** for millisecond-latency)
* **Vector Database:** **ChromaDB** for semantic indexing
* **Embeddings:** `all-MiniLM-L6-v2` (Sentence-Transformers)
* **Frontend:** **Streamlit**
* **Deployment Tunnel:** **Ngrok** (Stable production-grade tunneling)

## 🏗️ Architecture
1.  **Document Ingestion:** Users upload `.txt` files which are split into semantic chunks.
2.  **Vectorization:** Each chunk is converted into a high-dimensional vector.
3.  **Semantic Retrieval:** When a query is made, the system performs a similarity search in ChromaDB to find the most relevant context.
4.  **Contextual Generation:** The retrieved data is fed into the Llama model to ensure the response is 100% grounded in the document (Zero Hallucinations).

## 🔧 Challenges & Solutions
* **Quota Limits:** Initially built with Gemini, but pivoted to Groq to ensure 100% uptime and faster inference.
* **Deployment Hurdles:** Solved modular JavaScript fetch errors during tunneling by migrating from Localtunnel to Ngrok.

## 🏃 How to Run
1. Clone the repo:
   ```bash
   git clone [https://github.com/Nithya2405/NexusNote.git](https://github.com/Nithya2405/NexusNote.git)
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the app:
   ```bash
   streamlit run app.py
   ```

---
Built by **Nithyasundari S (Nithu)** *Artificial Intelligence & Machine Learning Engineering Student*
```

