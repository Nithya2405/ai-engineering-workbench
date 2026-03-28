# ai-engineering-workbench
A repository dedicated to exploring the implementation of Generative AI, focusing on moving models into production-ready environments.

## 🗺️ Project Roadmap

This table tracks the technical progression of the workbench, moving from basic model consumption to autonomous agentic workflows.

| Day | Module | Technical Implementation | Key Outcome |
| :--- | :--- | :--- | :--- |
| **01** | **Inference Basics** | Multi-provider benchmarking (GPT-4o vs Gemini 1.5) | Understood model latency & response variance |
| **02** | **Token Economics** | Built a Tiktoken-based counter & cost estimator | Optimized context window usage & API budgeting |
| **03** | **AI Safety** | Integrated OpenAI Moderation API for input filtering | Built a 'Security Layer' to block harmful prompts |
| **04** | **Embeddings** | Text-to-Vector conversion using `sentence-transformers` | Visualized semantic clusters in high-dimensional space |
| **05** | **Vector Storage** | Initialized ChromaDB for local document indexing | Created a persistent 'Memory' for unstructured data |
| **06** | **RAG Pipeline** | Contextual retrieval combined with Gemini 2.0 Flash | Eliminated hallucinations via fact-based grounding |
| **07** | **Prototyping** | Full-stack UI development using Streamlit | Built "NexusNote" for interactive document chat |
| **08** | **Tool Definition** | Tavily Search API integration for live web access | Overcame the LLM knowledge cutoff limitation |
| **09** | **Agentic Reasoning** | Implemented the ReAct (Reason + Act) Pattern | Enabled the model to plan steps before execution |
| **10** | **Function Calling** | Strict JSON schema contract for tool execution | Built a reliable, production-grade agentic interface |

---

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

