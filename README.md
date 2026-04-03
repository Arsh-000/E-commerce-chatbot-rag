# 🛍️ E-commerce Chatbot using GenAI (RAG + Semantic Routing)

**📌 Overview**

This project builds an intelligent E-commerce Chatbot powered by Large Language Models (LLMs) that can understand user intent and dynamically respond to queries.

The system combines:

- Vector-based retrieval (RAG) for FAQs
- SQL-based querying for product search
- Semantic routing for intent classification

This enables the chatbot to provide accurate, real-time, and context-aware responses.

**🎯 Problem Statement**

Traditional chatbots:

- Fail to understand user intent
- Cannot access structured product databases
- Provide generic or incorrect responses

This project solves these challenges by building a multi-chain GenAI system that routes queries intelligently.

**🧠 Solution Architecture**

The chatbot follows an intent-based routing architecture:

- User submits a query
- Semantic router identifies intent
- Query is routed to:
- FAQ Chain (RAG) → for policy/help queries
- SQL Chain → for product-related queries
- LLM generates the final response
  
**🔹 FAQ Chain (RAG)**

- Uses ChromaDB vector database
- Embeddings via Sentence Transformers
- Retrieves relevant context
- LLM generates answer grounded in context
  
**🔹 SQL Chain**

- Converts natural language → SQL query
- Executes query on SQLite database
- Formats result using LLM
  
**🔹 Semantic Router**

- Built using semantic-router library
- Classifies queries into:
- FAQ
- Product search
  
**🔹 LLM Layer**

Powered by LLaMA 3 via Groq API
Used for:

- Answer generation
- SQL generation
- Response formatting

**⚙️ Tech Stack**

- Python
- Groq (LLaMA 3)
- ChromaDB
- SQLite
- Semantic Router
- Sentence Transformers
- Streamlit

**📊 Features**

- Intent-based query routing
- FAQ answering using vector search
- Product search using natural language
- Real-time database querying
- Chat-based UI
  
**🖥️ Web Application**

- Built using Streamlit
- Chat-style interface
- Supports multi-type queries
  
**🚀 How to Run Locally**

git clone https://github.com/<your-username>/ecommerce-chatbot-rag.git
cd ecommerce-chatbot-rag
pip install -r app/requirements.txt

Create .env file:

GROQ_MODEL=llama-3.3-70b-versatile
GROQ_API_KEY=your_api_key

Run:

streamlit run app/main.py

## **📁 Project Structure**

```
ecommerce-chatbot-rag/
│
├── app/
│   ├── main.py
│   ├── faq.py
│   ├── sql.py
│   ├── router.py
│   ├── requirements.txt
│   │
│   └── resources/
│       ├── faq_data.csv
│       ├── ecommerce_data_final.csv
│       ├── architecture-diagram.png
│       └── product-ss.png
│
├── db.sqlite
├── csv_to_sqlite.py
├── README.md
```

**💡 Business Impact**

- Enhances customer support automation
- Improves product discovery experience
- Reduces manual query handling
- Scalable for real-world e-commerce platforms

**🔥 Key Highlights**

- Hybrid system (RAG + SQL + Routing)
- Real-world GenAI system design
- Uses LLM beyond text generation
- Production-style architecture

**🔮 Future Improvements**

- Add conversational memory
- Integrate recommendation engine
- Deploy using APIs (FastAPI)
- Add user personalization

**📌 Summary**

This project demonstrates how GenAI systems can combine structured and unstructured data sources to build intelligent, scalable applications for real-world use cases.


