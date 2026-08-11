<div align="center">

# Hi, I'm Nguyễn Cao Bản 👋

### AI Developer · RAG & LLM Applications · Software Engineering

**Building AI systems that go beyond demos — combining intelligent models, retrieval systems, and reliable backend engineering.**

[![GitHub](https://img.shields.io/badge/GitHub-caoban123-181717?style=for-the-badge\&logo=github)](https://github.com/caoban123)
[![Email](https://img.shields.io/badge/Email-caoban170106%40gmail.com-EA4335?style=for-the-badge\&logo=gmail\&logoColor=white)](mailto:caoban170106@gmail.com)
[![Facebook](https://img.shields.io/badge/Facebook-Nguyễn_Bản-1877F2?style=for-the-badge\&logo=facebook\&logoColor=white)](https://www.facebook.com/nguyen.ban.591323)

</div>

---

## 👨‍💻 About Me

I'm **Nguyễn Cao Bản**, an Artificial Intelligence student at the **University of Science, Vietnam National University Ho Chi Minh City (HCMUS)**.

My main interest lies at the intersection of **Artificial Intelligence and Software Engineering**. I enjoy turning AI concepts into practical applications — especially systems involving **Large Language Models, Retrieval-Augmented Generation (RAG), vector databases, and backend services**.

Rather than treating AI models as isolated components, I'm particularly interested in building the systems around them: **retrieval pipelines, memory architectures, APIs, streaming, deployment, evaluation, and reliability**.

Currently, I'm expanding my knowledge in **Deep Learning, Machine Learning, Computer Vision, Reinforcement Learning, and Knowledge Representation**, while continuously strengthening my foundations in algorithms and software development.

> **Current focus:** Building practical AI systems that can retrieve, reason, remember, and interact with users reliably.

---

## 🧠 Areas of Interest

`Artificial Intelligence` · `Generative AI` · `Large Language Models` · `RAG` · `AI Agents` · `Vector Search` · `Machine Learning` · `Deep Learning` · `Computer Vision` · `Backend Engineering`

---

## 🛠️ Tech Stack

### AI / Machine Learning

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square\&logo=python\&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square\&logo=pytorch\&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square\&logo=scikitlearn\&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square\&logo=numpy\&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square\&logo=pandas\&logoColor=white)

### LLM / RAG

![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square)
![LangGraph](https://img.shields.io/badge/LangGraph-Agentic_AI-1C3C3C?style=flat-square)
![Qdrant](https://img.shields.io/badge/Qdrant-DC244C?style=flat-square)
![ChromaDB](https://img.shields.io/badge/ChromaDB-Vector_DB-orange?style=flat-square)
![OpenAI](https://img.shields.io/badge/OpenAI_API-412991?style=flat-square\&logo=openai\&logoColor=white)
![Gemini](https://img.shields.io/badge/Gemini_API-8E75B2?style=flat-square\&logo=googlegemini\&logoColor=white)

### Backend / Web

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square\&logo=fastapi\&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square\&logo=javascript\&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square\&logo=html5\&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square\&logo=css3\&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-DD2C00?style=flat-square\&logo=firebase\&logoColor=white)

### Development & Deployment

![Git](https://img.shields.io/badge/Git-F05032?style=flat-square\&logo=git\&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square\&logo=github\&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square\&logo=docker\&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=flat-square\&logo=cloudflare\&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square\&logo=linux\&logoColor=black)

---

# 🚀 Featured Project

## 🌌 AI Story Adventure

### Generative AI · RAG · Vector Memory · FastAPI · LLM

**AI Story Adventure** is an AI-powered interactive storytelling and RPG platform designed to generate dynamic stories while maintaining long-term narrative consistency.

Unlike a simple chatbot that relies entirely on the current context window, the system implements a **semantic memory architecture** that retrieves relevant events from previous interactions and provides them back to the LLM as contextual memory.

🔗 **Repository:** [github.com/caoban123/aistoryadventure](https://github.com/caoban123/aistoryadventure)

### 🧠 AI & RAG Architecture

The application uses a **Retrieval-Augmented Generation pipeline** backed by **Qdrant / ChromaDB**.

Previous events are transformed into vector embeddings and stored as semantic memories. When the player performs a new action, the system retrieves the most relevant memories using **cosine similarity** and injects them into the LLM context.

This allows the AI to maintain consistency across long-running stories without continuously sending the entire conversation history.

### ⚙️ Backend Engineering

The backend is built with **FastAPI** and handles AI orchestration, authentication, game logic, memory retrieval, and API communication.

The system also uses **Server-Sent Events (SSE)** to stream generated responses to the client in real time, reducing perceived latency during LLM generation.

Background tasks are used for operations such as **memory summarization and vector storage**, preventing expensive AI operations from blocking the main request flow.

### 🔄 AI Provider Fallback

The system includes an AI provider fallback mechanism designed to improve reliability when an API reaches its quota or becomes temporarily unavailable.

It can dynamically route requests between providers such as:

`Gemini → OpenAI → Groq`

This allows the application to remain available even when individual model providers encounter failures.

### 🎮 Deterministic RPG Engine

Game mechanics such as **damage calculation, critical hits, inventory, attributes, and combat rules** are handled deterministically in Python.

The LLM is responsible for narrative generation rather than critical game-state calculations.

This separation helps prevent hallucinated game logic and makes the overall system more predictable.

### 🏗️ Architecture

```text
User
 │
 ▼
Frontend
 │
 ▼
FastAPI Backend
 │
 ├── Authentication
 │
 ├── RPG Engine
 │
 ├── Safety Layer
 │
 ├── RAG / Memory Retrieval
 │       │
 │       ▼
 │   Qdrant / ChromaDB
 │
 └── LLM Orchestrator
         │
         ├── Gemini
         ├── OpenAI
         └── Groq
              │
              ▼
        SSE Streaming
              │
              ▼
             User
```

### 🔧 Main Technologies

`Python` · `FastAPI` · `RAG` · `Qdrant` · `ChromaDB` · `Vector Embeddings` · `Gemini API` · `OpenAI API` · `Firebase Authentication` · `SSE` · `Docker` · `Coolify` · `Cloudflare Tunnel`

---

## 📚 Other Projects

### 🧩 Data Structures & Algorithms

**[DataStructureAndAlgorithms](https://github.com/caoban123/DataStructureAndAlgorithms)**

A collection of implementations and exercises focused on core **data structures, algorithms, problem-solving techniques, and computational thinking**.

---

### 🧠 LeetCode & NeetCode

**[LeetCode](https://github.com/caoban123/LeetCode)** · **[NeetCode](https://github.com/caoban123/NeetCode)**

My algorithm practice repositories where I study different approaches to solving programming problems and strengthen my foundations in **data structures, algorithms, and complexity analysis**.

---

### 🎮 Caro

**[Caro](https://github.com/caoban123/Caro)**

A Python implementation of the traditional **Gomoku/Caro** game, created as part of my journey in applying programming concepts to interactive applications.

---

## 📊 GitHub Activity

<div align="center">

![Bản's GitHub Stats](https://github-readme-stats.vercel.app/api?username=caoban123\&show_icons=true\&hide_border=true\&count_private=true\&theme=tokyonight)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=caoban123\&layout=compact\&hide_border=true\&theme=tokyonight)

</div>

---

## 🎯 What I'm Learning

At the moment, I'm focusing on developing a deeper understanding of:

**Deep Learning** — neural networks, optimization, CNNs, representation learning

**Machine Learning** — model development, evaluation, and classical ML techniques

**Computer Vision** — detection, segmentation, tracking, and visual representation learning

**LLM & RAG Systems** — retrieval, embeddings, vector databases, agents, memory, and evaluation

**Reinforcement Learning** — agents, policies, value functions, and sequential decision-making

**Algorithms & Data Structures** — improving problem-solving and software engineering fundamentals

---

## 🤝 Let's Connect

I'm always interested in discussing **AI, RAG, LLM applications, software engineering, research ideas, and interesting open-source projects**.

📧 **Email:** [caoban170106@gmail.com](mailto:caoban170106@gmail.com)

💻 **GitHub:** [github.com/caoban123](https://github.com/caoban123)

💬 **Facebook:** [Nguyễn Bản](https://www.facebook.com/nguyen.ban.591323)

---

<div align="center">

### Build. Learn. Improve. Repeat.

*"The best way to understand a system is to build one."*

⚡ Fun fact: My code works perfectly... **on the second run.** 😏

</div>
