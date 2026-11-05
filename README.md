# Hi, I'm Manish Jat 👋

**AI Engineer: I build production RAG systems, AI agents and LLM-powered backends.**
Co-founder of [VedQo](https://vedqo.in) · Rajasthan, India · Working with startups worldwide

[![Email](https://img.shields.io/badge/Email-hr.vedqo%40gmail.com-D14836?logo=gmail&logoColor=white)](mailto:hr.vedqo@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-jatmanis11-0077B5?logo=linkedin&logoColor=white)](https://linkedin.com/in/jatmanis11)
[![X](https://img.shields.io/badge/X-jatmanis1-black?logo=x&logoColor=white)](https://x.com/jatmanis1)

---

## What I can build for you

- **Chat over your data (RAG):** answers grounded in your documents, with citations, hybrid search and multi-tenant isolation
- **AI agents:** tool-using LLM workflows that automate support, ops and back-office tasks
- **Custom models and fast inference APIs:** fine-tuning, ONNX optimisation, FastAPI serving
- **Full AI products:** together with my co-founder (full-stack), from idea to a deployed MVP

Have an AI feature on your roadmap? **[Email me](mailto:hr.vedqo@gmail.com)** with a short description and I'll reply within 24 hours.

---

## Featured work

### 📄 DocMind: document Q&A with exact citations
[Live demo](https://docmind-frontend-two.vercel.app/) · [Backend](https://github.com/jatmxai-lab/docmind) · [Frontend](https://github.com/jatmxai/docmind-frontend)

Upload PDFs, CSVs, Word documents or images and ask questions. Answers stream token by token, with citations to the exact page or row.

- Hybrid retrieval (vector + BM25) over per-user Pinecone namespaces for tenant isolation
- Multimodal ingestion with Gemini, so images are handled without a separate OCR step
- Semantic caching and server-enforced quotas in Redis, with automatic refunds on failed uploads
- API-key rotation with cooldown on HTTP 429 and graceful degradation under rate limits
- Built to run on serverless Postgres: transaction pooler, migrations on boot, scales to zero

`FastAPI` `Gemini` `Pinecone` `Postgres` `Redis` `React` `Cloud Run` `GitHub Actions`

### 🛡️ SentinelLM: fine-tuned toxicity classifier, 2.56× faster on CPU
[Live demo](https://huggingface.co/spaces/jatmanis1/sentinellm-space) · [API docs](https://jatmanis1-sentinellm-space.hf.space/docs) · [Model card](https://huggingface.co/jatmanis1/sentinellm-v1) · [Code](https://github.com/jatmxai-lab/sentinellm)

DistilBERT fine-tuned on Civil Comments, exported to ONNX and served behind an async API.

- **F1 0.89 · accuracy 0.94** on a stratified validation set
- **p50 latency 24.8 ms → 9.7 ms** after the ONNX export
- A rule-based pre-filter catches known jailbreak patterns in about 1 ms, before the model runs
- Redis cache for repeated inputs; every prediction logged to Postgres

`PyTorch` `Transformers` `ONNX Runtime` `FastAPI` `Redis` `Hugging Face`

### ⚡ Rate limiter: multi-tenant rate limiting with ML anomaly detection
[Code and docs](https://github.com/jatmxai-lab/rate-limiter)

A standalone rate-limiting service for FastAPI, Django and Express apps, with a live traffic dashboard.

- 4 algorithms (sliding window, token bucket, fixed window, leaky bucket), each atomic through a Redis Lua script
- Hot path in Redis, durable config and history in Postgres
- Isolation Forest flags scraping, credential stuffing and traffic spikes, then sends a webhook alert to the tenant
- Python SDK with a 3-line FastAPI integration; pytest suite in CI; documentation site built with MkDocs

`FastAPI` `Redis Lua` `Postgres` `scikit-learn` `React` `WebSocket` `Cloud Run`

### 🧑‍💼 VedQo: AI candidate screening for recruiters
[vedqo.in](https://vedqo.in)

My current product. It helps recruiters shortlist candidates faster with AI-scored assessments and JD-to-candidate matching. Pilots are running with recruiters in Rajasthan.

`Next.js` `Supabase` `pgvector` `Claude API`

---

## Stack

**AI / ML:** LangChain · OpenAI · Anthropic · Gemini · PyTorch · Transformers · ONNX · scikit-learn · Pinecone · pgvector
**Backend:** Python · FastAPI · Postgres · Redis · Celery · WebSockets
**Frontend:** Next.js · React · Vue
**Infra:** Docker · Google Cloud Run · Vercel · GitHub Actions · Hugging Face Spaces
