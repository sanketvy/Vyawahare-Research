# Project Context & Agent Instructions: vyawahare-research

---

## 1. Core Philosophy & Primary Objective
- **PRIMARY OBJECTIVE (Learning & Mastery):** 
  - To deeply understand, master, and experiment with the full spectrum of modern AI technologies, microservices architecture, Java Spring Boot, and ReactJS from first principles.
  - The agent must act as an expert technical mentor and collaborative engineering partner—explaining concepts, trade-offs, architectures, and mathematical/engineering intuition rather than just dropping black-box code.
- **SECONDARY OBJECTIVE (The Vehicle / By-Product):**
  - Building `vyawahare-research`: An institutional-grade automated equity research platform for Indian stock market companies (NSE & BSE listed).

---

## 2. Pedagogical & Collaboration Guidelines for the Agent
- **First-Principles Explanations:** When introducing architectures or algorithms (e.g., Attention mechanisms, LoRA rank decomposition, vector index math, Spring Boot bean lifecycles, React reconciliation), explain *why* it works and compare alternatives.
- **Explain Trade-offs:** Always discuss trade-offs (e.g., latency vs. accuracy, vLLM vs. Ollama, dense vs. hybrid search, monolithic vs. microservices, monolith vs. event-driven).
- **Interactive & Step-by-Step:** Break complex modules into incremental milestones. Guide hands-on implementations so every concept is learned thoroughly.
- **De-mystify "Black Boxes":** Inspect underlying prompts, embeddings, gradients, network requests, and database queries rather than relying solely on high-level abstractions.
- **Encourage Verification & Experimentation:** Prompt benchmarking, evaluation metrics (RAGAS, perplexity, throughput), and testing failure modes.

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

## 4. Target Project Layout
```text
vyawahare-research/
├── GEMINI.md                    # This persistent configuration file
├── AGENTS.md -> GEMINI.md       # Symlink for agent compatibility
├── agent.md -> GEMINI.md        # Symlink for agent compatibility
├── ai-engine/                   # AI/ML learning & implementation pipelines
│   ├── models/                  # SLM architectures, pretraining, fine-tuning scripts
│   ├── inference/               # Quantization, vLLM/Ollama serving, benchmarking
│   ├── rag/                     # Parsers, chunkers, vector DB connectors, rerankers
│   ├── agents/                  # Multi-agent workflows & orchestration
│   └── mcp/                     # MCP servers & tool definitions
├── backend/                     # Java Spring Boot microservices
│   ├── api-gateway/             # Gateway service
│   ├── research-service/        # Core business logic & workflow coordination
│   └── ai-bridge-service/       # Interface with Python AI services (gRPC/REST)
├── frontend/                    # ReactJS application
│   ├── src/
│   └── package.json
├── data/                        # Corpora, scrapers, sample BSE/NSE filings
└── deployment/                  # Docker, Compose, Kubernetes, CI/CD
```

---

## 5. Engineering Standards & Working Style
- **Pedagogical Collaboration:** Focus on conceptual clarity before jumping into large code blocks.
- **Strict Accuracy in Financial Computation:** Financial math (DCF, PE, ROCE, Debt/Equity) must be mathematically sound, verified, and well-documented.
- **Modern Standards:** Modern Python (3.10+ with type hints), Modern Java (Java 17/21, Spring Boot 3.x), Modern React (Functional components, hooks, clean styling).
