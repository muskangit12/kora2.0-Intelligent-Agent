# Kora 2.0 – Intelligent Agent Platform

Kora 2.0 is a modular, agentic AI system built using [LangGraph](https://github.com/langchain-ai/langgraph), designed to support intelligent conversations with persistent memory, internet-accessible responses, and real-time streaming capabilities. This platform demonstrates how to orchestrate multiple tools and services to build production-ready conversational agents.


**Kora2.0** - https://kora2-0.onrender.com/

---

## 🚀 Features

- **Agent Framework with LangGraph**  
  Implements an agent-based reasoning loop using LangGraph to support complex workflows, tool usage, and memory-aware interactions.

- **Persistent Memory with MongoDB**  
  Agent memory is persisted using a custom LangGraph `checkpointer`, backed by MongoDB. This enables context-aware interactions across sessions and long-form reasoning.

- **Internet-Connected Agent (RAG)**  
  Integrated [Tavily Search API](https://docs.tavily.com/) to enable Retrieval-Augmented Generation (RAG), allowing the agent to query the internet for up-to-date information.

- **Real-Time Streaming with Server-Sent Events (SSE)**  
  The agent streams partial responses to the frontend using SSE, improving user experience by reducing perceived latency.

- **API Development with FastAPI**  
  Built a robust, async-capable API layer using FastAPI to interface with the agent, stream responses, and expose health/debug routes.

- **Containerization with Docker**  
  The application is fully containerized using Docker, making it easy to deploy locally or to cloud services.

---
## Screenshots

<img width="500" height="580" alt="image" src="https://github.com/user-attachments/assets/49080785-c522-4507-8afc-17a415b44841" />
<img width="500" height="580" alt="Screenshot 2026-03-03 182825" src="https://github.com/user-attachments/assets/759b2899-ad0b-4dfc-b436-a20b153499ba" />

<img width="500" height="580" alt="image" src="https://github.com/user-attachments/assets/45e2ecf0-9763-4500-a6c0-bea3f0d48e7d" />
<img width="500" height="581" alt="image" src="https://github.com/user-attachments/assets/4da0bd9c-30e8-43ff-a905-643a70141646" />


## 🧠 Architecture Overview

Client (Web UI)
│
└──▶ FastAPI (SSE + REST)
│
├──▶ LangGraph Agent
│ ├── Memory Checkpointer (MongoDB)
│ └── Tools (Tavily Search)
│
└──▶ Streamed Response Handler (SSE)

## 📦 Tech Stack

- **LangGraph** – Agent orchestration
- **FastAPI** – API server with async capabilities
- **MongoDB** – Memory persistence via checkpointing
- **Tavily Search** – Web-connected data retrieval
- **Server-Sent Events (SSE)** – Real-time streaming
- **Docker** – Containerized deployment

  ## 🛠️ Getting Started

### Prerequisites

- Python 3.10+
- Docker (optional for deployment)
- MongoDB instance (local or cloud)
- Tavily API Key

### Installation

```bash
git clone https://github.com/sansosho-g/kora-2.0.git
cd kora-2.0
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows
pip install -r requirements.txt




