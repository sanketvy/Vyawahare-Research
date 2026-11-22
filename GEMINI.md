# Project Context & Agent Instructions: vyawahare-research

---

## 1. Core Philosophy & Primary Objective
- **PRIMARY OBJECTIVE (Interview Mastery & Cracking Tech Interviews):** 
  - The single overriding objective is to **crack top-tier technical interviews** (Senior/Staff Software Engineer, Backend Distributed Systems, and Applied AI/ML Engineer).
  - Every concept, pattern, and line of code must be taught through the lens of how it is questioned and evaluated in real tech interviews (Google, Meta, Uber, tier-1 tech firms, quantitative hedge funds).
- **SECONDARY OBJECTIVE (The Vehicle / Portfolio):**
  - Building `vyawahare-research`: An institutional-grade automated equity research platform for Indian stock market companies (NSE & BSE listed) serving as proof-of-work.

---

## 2. Interview-First Pedagogical Guidelines for the Agent
- **NO Academic Math Proofs or Derivations:** 
  - Software and AI systems interviewers NEVER ask for pencil-and-paper variance proofs, calculus derivations, or dense Greek letter math. 
  - Strictly avoid theoretical academic math dumps.
- **Focus on What Interviewers Actually Ask:**
  1. **Time & Space Complexity:** Always analyze big-$O$ complexity (e.g., why Attention is $O(N^2)$ in time/memory, how sequence length squares compute).
  2. **Memory & Production Bottlenecks:** Explain real resource limits (e.g., KV-cache memory formulas, why servers crash with Out of Memory (OOM), memory bandwidth vs. compute-bound operations).
  3. **Architecture Trade-offs & Alternatives:** Always frame decisions as trade-offs (e.g., MHA vs. GQA vs. MQA, dense vs. hybrid search with Reciprocal Rank Fusion, gRPC vs. REST, Kafka vs. RabbitMQ).
  4. **Production Gotchas & Failure Modes:** Highlight what breaks in production and how senior engineers mitigate it (e.g., rate limits, connection pools, cache stampedes, causal masking to prevent training leakage).
- **Explanation Structure (How to Explain Every Topic):**
  - **The Intuitive Mechanism:** Explain what is happening mechanically in plain, clear English.
  - **The Real Industry & Theory Terminology:** Map the mechanism directly to the exact terms interviewers use (Embeddings, Attention Logits, Softmax, Projections, KV-Cache).
  - **The Interviewer Drill:** Frame the topic around: *"If an interviewer asks X, here is the crisp 60-second answer, followed by the deep-dive trade-off defense."*
- **No Baby Talk & No Dense Math:** Strike the gold standard: clear, conceptual intuition married directly to real-world software engineering and system architecture terminology.

---

## 3. Learning & Technical Roadmap

### A. AI & Machine Learning Engineering (Deep Exploration)
1. **Foundations & Architecture:** Transformer architectures, tokenization (Byte-Pair Encoding for financial terms), attention variants (MHA, GQA, FlashAttention).
2. **Small Language Models (SLMs):** Designing, training, and running efficient SLMs tailored for domain-specific tabular and financial extraction.
3. **Pretraining & Continued Pretraining:** Data curation, deduplication, tokenization pipelines, pretraining loops on Indian financial corpora (SEBI filings, concalls, annual reports).
4. **Fine-Tuning:**
   - Supervised Fine-Tuning (SFT) for instruction-following.
   - Parameter-Efficient Fine-Tuning (PEFT): LoRA, QLoRA, prefix tuning.
   - Alignment: DPO (Direct Preference Optimization) / RLHF for financial accuracy and tone.
5. **Inference Engineering:**
   - Engines: vLLM, TensorRT-LLM, Ollama, HuggingFace TGI.
   - Quantization: GGUF, AWQ, GPTQ, bitsandbytes (INT8/INT4).
   - Optimization: KV-cache management, speculative decoding, continuous batching.
6. **Context Engineering:** Dynamic prompt assembly, prompt caching, long-context handling, JSON/structured output enforcement (e.g., Outlines, Instructor).
7. **RAG & Vector Databases:**
   - Document chunking strategies (table-aware, semantic chunking for financial statements).
   - Vector Databases: Qdrant, Milvus, Chroma, pgvector.
   - Retrieval: Hybrid search (dense + BM25/sparse), cross-encoder rerankers, semantic caching, metadata filtering.
8. **Model Context Protocol (MCP) & Tool Use:**
   - Standardizing tool calls for BSE/NSE scrapers, market tickers, and financial ratio calculators.
9. **Multi-Agent Systems:**
   - Orchestration frameworks and agent patterns (reflection, planning, tool usage, multi-agent debate).
   - Specialized agents: Data Collector, Financial Analyst, Forensics Auditor, Report Synthesizer.

### B. Microservices & Enterprise Backend (Java Spring Boot)
1. **Spring Boot 3.x Deep Dive:** Inversion of Control (IoC), Dependency Injection (DI), Spring Security, Spring Data JPA/Hibernate.
2. **Microservices Architecture:**
   - Service discovery, API Gateway, configuration management.
   - Inter-service communication: Synchronous (REST, gRPC) and Asynchronous / Event-driven (Kafka / RabbitMQ).
   - Bridging Java backend with Python AI inference engines (gRPC/Protobuf, REST, async queues).
3. **Resilience & Scalability:** Circuit breakers (Resilience4j), rate limiting, distributed caching (Redis), distributed tracing.
4. **Scheduling & Pipelines:** Quartz/Spring Scheduler for automated earnings season ingestion workflows.

### C. Modern Frontend Engineering (ReactJS)
1. **React Fundamentals to Advanced:** Component lifecycle, hooks (`useEffect`, `useMemo`, `useCallback`, custom hooks), state management (Zustand/Redux Toolkit/TanStack Query).
2. **Financial Visualization & UI:**
   - Real-time stock charts, interactive financial statements, balance sheet tree views.
   - Interactive PDF research report viewer, markdown rendering with LaTeX math for valuation formulas.
3. **Real-Time Agent Streams:** Server-Sent Events (SSE) and WebSockets for real-time agent thought logs and streaming report generation.

### D. MLOps, DevOps & Deployment
1. Containerization (Docker multi-stage builds).
2. Orchestration (Docker Compose, Kubernetes basics).
3. Experiment tracking & model registry (MLflow, Weights & Biases).
4. CI/CD pipelines and deployment strategies.

---

## 4. Repository Structure
```text
vyawahare-research/
├── GEMINI.md                    # This persistent configuration file
├── AGENTS.md -> GEMINI.md       # Symlink for agent compatibility
├── agent.md -> GEMINI.md        # Symlink for agent compatibility
├── learning/                    # 🎓 Knowledge Base, Concept Notes & Interview Goldmine
├── frontend/                    # ReactJS application (UI, financial charts, live agent streams)
├── backend/                     # Java Spring Boot enterprise microservices & Python AI bridge
├── infrastructure/              # Docker, Docker Compose, Kubernetes, CI/CD deployment configs
├── research/                    # Indian market domain knowledge, SEBI filings, financial & forensic models
├── playground/                  # Rapid prototyping sandbox, scratch scripts, notebooks, exploratory lab
└── technology/                  # Deep-dive AI/ML implementations (SLMs, pretraining, fine-tuning, RAG, agents, MCP)
```

---

## 5. Engineering Standards & Working Style
- **Pedagogical Collaboration:** Focus on conceptual clarity before jumping into large code blocks.
- **Strict Accuracy in Financial Computation:** Financial math (DCF, PE, ROCE, Debt/Equity) must be mathematically sound, verified, and well-documented.
- **Modern Standards:** Modern Python (3.10+ with type hints), Modern Java (Java 17/21, Spring Boot 3.x), Modern React (Functional components, hooks, clean styling).
