
<h1 align="center">Hi 👋, I'm Manish Jat</h1>
<h3 align="center">Backend + AI Engineer | Production LLM Systems | Distributed Systems</h3>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=jatmxai&label=Profile%20views&color=0e75b6&style=flat" alt="jatmxai" />
</p>

---

🚀 Building **production-grade AI systems** that scale — RAG pipelines, ML model serving, and backend infrastructure  
🧠 Expertise in **LangChain, FastAPI, PostgreSQL, Redis, Pinecone, and vector databases**  
🔧 I don't just call LLM APIs — I understand **both backend architecture AND AI/ML systems**  
👯 Looking to collaborate on **RAG systems, AI infrastructure, and full-stack AI applications**  

---


## 💬 **Core Skills for Backend + AI Engineer**

| Skill Area                      | Level                    | Tools & Tech |
|---------------------------------|--------------------------|--------------|
| **Backend API Development**     | ⭐⭐⭐⭐⭐ (Expert) | FastAPI, async/await, REST APIs, GraphQL, JWT auth |
| **Database Design & Optimization** | ⭐⭐⭐⭐ (Advanced) | PostgreSQL, Redis, vector databases (Pinecone, Chroma), TimescaleDB |
| **LLM Integration & RAG**       | ⭐⭐⭐⭐⭐ (Expert) | LangChain, embeddings, hybrid search, LLM orchestration, OpenAI, Anthropic |
| **ML Model Training & Optimization** | ⭐⭐⭐⭐ (Advanced) | PyTorch, DistilBERT, ONNX optimization, fine-tuning, MLflow |
| **Distributed Systems & Caching** | ⭐⭐⭐⭐ (Advanced) | Redis, Redis Lua scripts, rate limiting, anomaly detection |
| **Async & Real-time Systems**  | ⭐⭐⭐⭐ (Advanced) | Celery, async workers, WebSockets, message queues |
| **Data Processing Pipelines**   | ⭐⭐⭐⭐ (Advanced) | Batch processing, ETL, document ingestion, streaming |
| **Monitoring & MLOps**          | ⭐⭐⭐⭐ (Advanced) | TimescaleDB, metrics collection, drift detection, dashboards, alerting |
| **Full-Stack Integration**      | ⭐⭐⭐⭐ (Advanced) | Next.js, Vue.js, Docker, GitHub Actions CI/CD |
| **Python Engineering**          | ⭐⭐⭐⭐⭐ (Expert) | Type hints, async patterns, testing, production code quality |

---

## 🚀 Flagship Projects (Backend + AI Engineer)

> 🚀 *Production-grade AI systems demonstrating backend architecture, LLM engineering, and full-stack deployment.*

---

### 1️⃣ **DocMind** — Production RAG System ✅ LIVE
> 🧠 *Multi-tenant AI Document Intelligence Platform*

<p align="center">
  <img src="https://img.shields.io/badge/Status-DEPLOYED-brightgreen?style=for-the-badge" />
  <img src="https://img.shields.io/badge/FastAPI-00C8DF?style=for-the-badge&logo=fastapi" />
  <img src="https://img.shields.io/badge/Gemini%202.5-4285F4?style=for-the-badge&logo=google" />
  <img src="https://img.shields.io/badge/Pinecone-2E3838?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Cloud%20Run-4285F4?style=for-the-badge&logo=google-cloud" />
  <img src="https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel" />
</p>

**[🔗 Try Live Demo](https://docmind-frontend-two.vercel.app/)** · [Frontend Repo](https://github.com/jatmxai/docmind-frontend) · [Deploy Guide](https://github.com/jatmxai/docmind/blob/main/DEPLOY.md)

Upload any document (PDF, CSV, DOCX, images) → Ask questions → Get **streaming answers with citations to exact pages/rows**.

**What It Does:**
- 📄 Multi-format document ingestion (PDF, CSV, DOCX, PNG/JPG)
- 🔍 Hybrid search (Vector embeddings + BM25 keyword search)
- 🤖 Multi-step reasoning with tool use
- 💾 Semantic caching + quota management (Redis)
- 📊 Citation tracking (exact page/row references)
- 🔐 Multi-tenant with JWT auth + per-user Pinecone namespaces

**Engineering Highlights:**
- ✅ **18-key Gemini pool** with round-robin + cooldown for rate-limit survival
- ✅ **PgBouncer-safe asyncpg** (UUID-named prepared statements for stale connection safety)
- ✅ **Matryoshka embedding truncation** (3072→768 dims, preserves cosine similarity)
- ✅ **Server-Sent Events** for token-by-token streaming
- ✅ Alembic migrations on container boot (scales to zero)

🧰 **Tech Stack:** FastAPI, Gemini 2.5 Flash, Pinecone, Supabase (Postgres + Storage), Upstash Redis, Next.js + React, Cloud Run, GitHub Actions  
📊 **Cost:** ~$5/month (free tiers + minimal paid)

🔧 **Status:** ✅ **DEPLOYED** — fully functional, live users

---

### 2️⃣ **SentinelLM** — ML Model + Production API ✅ LIVE
> 🧠 *Fine-tuned Toxicity Classifier with ONNX Acceleration*

<p align="center">
  <img src="https://img.shields.io/badge/Status-DEPLOYED-brightgreen?style=for-the-badge" />
  <img src="https://img.shields.io/badge/DistilBERT-FF6B6B?style=for-the-badge" />
  <img src="https://img.shields.io/badge/ONNX%202.56x-005CED?style=for-the-badge" />
  <img src="https://img.shields.io/badge/FastAPI-00C8DF?style=for-the-badge&logo=fastapi" />
  <img src="https://img.shields.io/badge/HuggingFace%20Spaces-FFD21E?style=for-the-badge&logo=huggingface" />
  <img src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis" />
</p>

**[🔗 Live API + Demo](https://huggingface.co/spaces/jatmanis1/sentinellm-space)** · [API Docs](https://jatmanis1-sentinellm-space.hf.space/docs) · [Model Card](https://huggingface.co/jatmanis1/sentinellm-v1)

Fine-tuned **DistilBERT** for toxicity detection. Optimized to **ONNX for 2.56x faster CPU inference**. Deployed with async **FastAPI**, **exact-match Redis cache**, rule-based fast-path, and Postgres logging.

**What It Does:**
- 🧠 Binary toxicity classification (clean vs. toxic)
- ⚡ ONNX optimization: PyTorch 24.8ms → ONNX 9.7ms p50 latency
- 🚨 Rule pre-filter layer for jailbreak patterns (~1ms, deterministic)
- 💾 Redis exact-match cache (99%+ hit rate for repeated inputs)
- 📊 Prediction logging to Postgres
- 🎯 JSON API + Gradio UI

**Engineering Highlights:**
- ✅ **2.56x speedup** from ONNX (single-sample and batch-32)
- ✅ **Civil Comments dataset** (200k rows, stratified, unbiased sample)
- ✅ **F1 0.89, accuracy 0.94** on validation set
- ✅ **Rule layer short-circuits** known attack patterns before model inference
- ✅ **SQLite or Postgres** logging (works in Spaces or self-hosted)

🧰 **Tech Stack:** DistilBERT, PyTorch, ONNX Runtime, FastAPI, Redis, PostgreSQL/SQLite, HuggingFace Spaces  
📊 **Cost:** $0/month (free HF Spaces + optional Railway backend)

🔧 **Status:** ✅ **DEPLOYED** — 18 test cases, live inference

---

### 3️⃣ **API Rate Limiter** — Distributed Systems ⏳ COMING SOON
> ⚙️ *Intelligent Rate Limiting + Traffic Analytics + ML Anomaly Detection*

<p align="center">
  <img src="https://img.shields.io/badge/Status-BUILDING-orange?style=for-the-badge" />
  <img src="https://img.shields.io/badge/FastAPI-00C8DF?style=for-the-badge&logo=fastapi" />
  <img src="https://img.shields.io/badge/Redis%20Lua-DC382D?style=for-the-badge&logo=redis" />
  <img src="https://img.shields.io/badge/PostgreSQL-336791?style=for-the-badge&logo=postgresql" />
  <img src="https://img.shields.io/badge/WebSocket-010101?style=for-the-badge" />
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge" />
</p>

**4 rate limiting algorithms** backed by **Redis Lua scripts** for atomic operations. Real-time **WebSocket dashboard** + **Isolation Forest ML anomaly detection** for DDoS/scraper detection.

**What It Does:**
- 🔒 Token bucket, sliding window, fixed window, leaky bucket algorithms
- ⚛️ Redis Lua scripts for atomicity (prevents race conditions)
- 📊 Real-time traffic analytics via WebSocket
- 🚨 ML-based anomaly detection (DDoS, scrapers, traffic spikes)
- 🔔 Webhook alerting system
- 📈 Multi-tenant traffic logging in PostgreSQL

**Why It's Important:**
- ✅ Distributed systems thinking (algorithms, race conditions, atomicity)
- ✅ Production infrastructure patterns (Redis, WebSocket, monitoring)
- ✅ Understanding why Lua scripts matter in production

🧰 **Tech Stack:** FastAPI, Redis, PostgreSQL, Lua scripts, scikit-learn, WebSocket, Celery  
📊 **Timeline:** 5 weeks | **Plan:** [api_rate_limiter_plan.md](./portfolio%20projects/api_rate_limiter_plan.md)

🔧 **Status:** ⏳ **IN DEVELOPMENT** — [Demo link coming soon]

---

### 4️⃣ **DriftDetect** — LLM Monitoring & MLOps ⏳ COMING SOON
> 📊 *LLM Prompt Behavior Drift Detection with Time-Series Metrics*

**Continuously monitors LLM output quality** for semantic drift, tone shifts, factual consistency, and hallucination rates using sentence embeddings + LLM-as-judge evaluation.

**Features:**
- 🔄 Scheduled prompt execution (hourly/daily/weekly)
- 📊 Semantic similarity tracking vs baseline (TimescaleDB time-series)
- 🎯 Composite drift scoring (semantic, tone, factual, hallucination)
- 🤖 GPT-4o-mini LLM judge for evaluation
- 📈 Plotly Dash live dashboard
- 🔔 Webhook + email alerting
- Integrates with SentinelLM monitoring

🧰 **Tech Stack:** TimescaleDB, Celery beat, FastAPI, Plotly Dash, sentence-transformers, OpenAI  
📊 **Timeline:** 4 weeks | **Plan:** [driftdetect_plan.md](./portfolio%20projects/driftdetect_plan.md)

🔧 **Status:** ⏳ **PLANNED** — Coming after API Rate Limiter

---

## 🎁 Bonus Project

### 🤖 **AI Coding Agent** — Multi-Model LLM Orchestration ⭐⭐
> 🧠 *Claude Code Equivalent: Multi-Modal Reasoning with Tool Use*

<p align="center">
  <img src="https://img.shields.io/badge/Gemini%20API-4285F4?style=for-the-badge&logo=google&logoColor=white" />
  <img src="https://img.shields.io/badge/FastAPI-00C8DF?style=for-the-badge&logo=fastapi" />
  <img src="https://img.shields.io/badge/WebSocket-010101?style=for-the-badge" />
  <img src="https://img.shields.io/badge/VS%20Code%20Extension-007ACC?style=for-the-badge&logo=visualstudiocode" />
  <img src="https://img.shields.io/badge/Multi--Platform-FF6B6B?style=for-the-badge" />
</p>

A **self-built Claude Code equivalent** powered by Google's Gemini API. Multi-model pipeline with separate **Planner**, **Critic**, and **Reviewer** models. 48+ built-in tools (file I/O, shell, Git, browser, AST analysis). Available on **Web UI, VS Code extension, Telegram, and CLI**.

**What It Does:**
- 🧠 Multi-model reasoning (Planner → Critic → Reviewer)
- 🛠️ 48 built-in tools (parallel execution)
- 🔄 Snapshot/rollback for destructive operations
- 💡 Confidence gate (blocks risky actions)
- 🌐 WebSocket real-time updates
- 📦 VS Code extension + Telegram bot integration
- 🔌 MCP (Model Context Protocol) support

**Why It's Impressive:**
- ✅ Shows **deep LLM system design** (multi-model orchestration, tool use)
- ✅ **Multi-platform deployment** (web, extension, chat, CLI)
- ✅ Advanced patterns (snapshot/rollback, confidence gates)

🧰 **Tech Stack:** Gemini API, FastAPI, WebSocket, VS Code Extension API, Telegram SDK  
📊 **Outcome:** **LLM engineering maturity** — not just using APIs, but orchestrating them

---

## ✨ Project Status Overview

| 🎯 Project | Status | Focus | Stack Highlight |
|-----------|--------|-------|-----------------|
| **DocMind** | ✅ **LIVE** | Production RAG | Gemini + Pinecone + Cloud Run |
| **SentinelLM** | ✅ **LIVE** | ML + Serving | DistilBERT + ONNX (2.56x) + HF Spaces |
| **API Rate Limiter** | ⏳ BUILDING | Distributed Systems | Redis Lua + WebSocket + Anomaly Detection |
| **DriftDetect** | 🔄 PLANNED | MLOps & Monitoring | TimescaleDB + Celery + LLM Judge |
| **AI Coding Agent** | ⚡ ACTIVE | LLM Orchestration | Multi-model + Tool Use + Multi-platform |

**Completed: 2/4 Flagship Projects** ✅  
**In Progress: 1/4** ⏳  
**Planned: 1/4** 🔄

---



# 💻 Tech Stack — Backend + AI Engineer

**Core Languages**  
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)
![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white)
![Bash](https://img.shields.io/badge/bash_script-%23121011.svg?style=for-the-badge&logo=gnu-bash&logoColor=white)

**Backend & API Frameworks**  
![FastAPI](https://img.shields.io/badge/FastAPI-00C8DF?style=for-the-badge&logo=fastapi)
![Django](https://img.shields.io/badge/django-%23092E20.svg?style=for-the-badge&logo=django&logoColor=white)
![Flask](https://img.shields.io/badge/flask-%23000.svg?style=for-the-badge&logo=flask&logoColor=white)

**Databases & Data Storage**  
![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![TimescaleDB](https://img.shields.io/badge/TimescaleDB-0F7B99?style=for-the-badge)
![Pinecone](https://img.shields.io/badge/Pinecone-2E3838?style=for-the-badge)
![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white)

**LLM & AI Frameworks**  
![LangChain](https://img.shields.io/badge/LangChain-00A67E?style=for-the-badge&logo=chainlink&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FF9B00?style=for-the-badge&logo=huggingface&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![Anthropic](https://img.shields.io/badge/Anthropic-6C7F7C?style=for-the-badge)

**ML Engineering & Data Science**  
![Scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![ONNX](https://img.shields.io/badge/ONNX-005CED?style=for-the-badge)
![MLflow](https://img.shields.io/badge/MLflow-0194E2?style=for-the-badge)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)

**Async & Task Queues**  
![Celery](https://img.shields.io/badge/Celery-37B24D?style=for-the-badge)
![RabbitMQ](https://img.shields.io/badge/RabbitMQ-FF6B00?style=for-the-badge&logo=rabbitmq&logoColor=white)

**Frontend & Dashboards**  
![Next.js](https://img.shields.io/badge/next.js-%23000000.svg?style=for-the-badge&logo=next.js&logoColor=white)
![Vue.js](https://img.shields.io/badge/vue.js-%2335495e.svg?style=for-the-badge&logo=vuedotjs&logoColor=%234FC08D)
![Plotly](https://img.shields.io/badge/Plotly-3F4F75?style=for-the-badge&logo=plotly&logoColor=white)

**DevOps & Deployment**  
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![Railway](https://img.shields.io/badge/Railway-0B0D0E?style=for-the-badge&logo=railway)
![Vercel](https://img.shields.io/badge/vercel-%23000000.svg?style=for-the-badge&logo=vercel&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)

---

# 📊 GitHub Stats
<p>
  <img align="left" src="https://github-readme-stats.vercel.app/api/top-langs?username=jatmxai&show_icons=true&locale=en&layout=compact" alt="jatmxai" />
</p>

<p>
  &nbsp;<img align="center" src="https://github-readme-stats.vercel.app/api?username=jatmxai&show_icons=true&locale=en" alt="jatmxai" />
</p>

<p>
  <img align="center" src="https://github-readme-streak-stats.herokuapp.com/?user=jatmxai&" alt="jatmxai" />
</p>

---

### 🏆 GitHub Trophies
[![trophy](https://github-profile-trophy.vercel.app/?username=jatmxai&theme=flat&row=1&margin-w=15)](https://github.com/ryo-ma/github-profile-trophy)

---



## 🌐 Connect With Me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://linkedin.com/in/jatmanis11)
[![GitHub](https://img.shields.io/badge/GitHub-%23121011.svg?logo=github&logoColor=white)](https://github.com/jatmxai)
[![Email](https://img.shields.io/badge/Email-D14836?logo=gmail&logoColor=white)](mailto:hr.vedqo@gmail.com)
[![Twitter/X](https://img.shields.io/badge/X-black.svg?logo=X&logoColor=white)](https://x.com/jatmanis1)
[![Medium](https://img.shields.io/badge/Medium-12100E?logo=medium&logoColor=white)](https://medium.com/@jatmanis1)

---

## 🎯 What's Next?

I'm actively building the **4-project Backend + AI Engineer portfolio** (16 weeks). Starting with **API Rate Limiter** to build foundation, then **SentinelLM**, **DriftDetect**, and finally **DocMind** as the flagship system.

Looking for opportunities to work on **production LLM systems, RAG infrastructure, or full-stack AI applications**.

---

[![](https://visitcount.itsvg.in/api?id=jatmxai&icon=0&color=0)](https://visitcount.itsvg.in)
