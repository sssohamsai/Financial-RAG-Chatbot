# 🧠 Financial RAG Chatbot (Built on Screener Data)

Hi, I have created this chatbot by implementing **Retrieval-Augmented Generation (RAG)** on company financial data scraped from [Screener.in](https://www.screener.in/). Please enjoy the ride through this chatbot 🚂

It lets you ask natural questions like:
> What is the ROE of Infosys in 2024?  
> Who had the average net profit in last 3 quarters for Tata Steel?  
> What is the 5-year EPS growth of Marico?

---

## 📆 WEEK 1: The First Station 🛤️

This week I learned about all the amazing ways your AI bot can understand *text* — whether you're talking about "how cool you are" or just yapping random stuff like *you usually do* 😂

I explored:
- **TF-IDF**
- **BM-25**
- **GloVe embeddings**
- Why these matter for vector search & information retrieval

📁 Check `resources/` for slides, notes & reference links

---

## 🧪 WEEK 2: Getting Hands Dirty with RAG

So this is when things got serious.

RAG isn’t just another 3-letter buzzword — it's the bridge that lets a language model answer questions about **data it was never trained on**.  
Imagine ChatGPT suddenly knowing all your boring Excel files — yeah, that's RAG.

I explored:
- How to split queries into subqueries
- How to chunk and embed structured financial data
- How to connect retriever + LLM for dynamic answers

📎 Here's a playground Colab where I tested RAG in Python:  
👉 [Colab: Playing with RAG](https://colab.research.google.com/drive/1HTPq8iUzDUpg-jzoBB8_tCw_tpH77gMm?usp=sharing)

---

## 🚀 WEEK 3–5: Implementation Phase

This is where I built the entire pipeline — from scratch.

#### ✅ Features
- Uses **Fin-MPNET** embeddings trained on financial text
- Embeds data extracted from Screener's Excel format
- Stores vectors in **Qdrant** (via Docker)
- Splits complex queries into **smart subqueries** using Mistral via Ollama
- Retrieves top-k relevant chunks for each subquery
- Assembles the final context
- Generates answers via **Mistral LLM**

---

## ⚙️ Installation & Setup

### 💾 Prerequisites (Install manually):
- **Docker** → [Get Docker](https://www.docker.com/get-started)
- **Ollama (for LLM)** → [Get Ollama](https://ollama.com/download)

---

### 🧠 Run the bot

Clone the repo and run:
```bash
python run_this.py
