# ai-engineering-workbench
A repository dedicated to exploring the implementation of Generative AI, focusing on moving models into production-ready environments.

## 🗺️ Project Roadmap
Day,Project Module,Technical Focus,Core Achievement
01,Model Benchmarking,LLM Inference,Compared GPT-4o vs Gemini 1.5 for cost/latency.
02,Token Analytics,Tokenization & Costing,Built a utility to estimate API pricing using tiktoken.
03,AI Safety,Input Moderation,"Implemented a ""Gatekeeper"" using OpenAI’s Moderation API."
04,Embeddings Lab,Vector Math,Converted college subjects into 384D semantic vectors.
05,Vector DB,Persistent Memory,Indexed high-dimensional data into ChromaDB.
06,RAG Pipeline,Context Augmentation,"Built a ""Chat with Docs"" flow using Gemini + ChromaDB."
07,Rapid Prototyping,UI/UX for AI,Deployed a full-stack RAG app using Streamlit.
08,Tool Definition,Real-time Search,Integrated Tavily API to bypass LLM knowledge cutoffs.
09,ReAct Logic,Reasoning Loops,"Implemented a manual ""Think-Act-Observe"" cycle."
10,Function Calling,Structured Contracts,Replaced manual prompts with a strict Function Schema.



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

