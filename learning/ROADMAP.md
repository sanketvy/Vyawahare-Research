# 📋 Technical Curriculum & Concept Mastery Roadmap

Status Legend:
- ⚪ **Not Started**
- 🟡 **In Progress (Implementing / Studying)**
- 🟢 **Mastered & Grilled (Can defend from first principles in interviews)**

---

## Track 1: AI Engineering & Domain-Specific SLMs

| # | Topic | Key Deliverable / Concept | Status | Notes Link |
| :---: | :--- | :--- | :---: | :--- |
| **1.1** | **Transformer Foundations from Scratch** | Self-Attention math ($Q, K, V$), Scaled Dot-Product, Multi-Head Attention (MHA) vs Grouped-Query Attention (GQA) | ⚪ | `01-ai-and-ml/01-transformer-attention.md` |
| **1.2** | **Positional Encodings & RoPE** | Rotary Position Embeddings (RoPE) intuition, complex numbers in attention, context extrapolation | ⚪ | `01-ai-and-ml/02-rope-positional-embeddings.md` |
| **1.3** | **Tokenization & Byte-Pair Encoding** | Training a custom BPE tokenizer on Indian financial terms, handling currency (`₹`, `Crore`, `Lakh`), vocabulary bloat | ⚪ | `01-ai-and-ml/03-financial-bpe-tokenization.md` |
| **1.4** | **Building a Mini-SLM in PyTorch** | Implementing Decoder-only SLM (~50M–100M params), KV cache, causal masking | ⚪ | `01-ai-and-ml/04-mini-slm-architecture.md` |
| **1.5** | **Pretraining Loop & Optimization** | Learning rate schedules (Cosine with warmup), AdamW, gradient accumulation, mixed precision (FP16/BF16) | ⚪ | `01-ai-and-ml/05-pretraining-mechanics.md` |
| **1.6** | **Indian Financial Corpora Pipeline** | Scraping BSE/NSE annual reports, deduplication (MinHash LSH), cleaning tabular noise | ⚪ | `01-ai-and-ml/06-financial-data-curation.md` |
| **1.7** | **Fine-Tuning: SFT (Supervised Fine-Tuning)** | Chat templates, instruction masking, training for structured financial metric extraction | ⚪ | `01-ai-and-ml/07-supervised-fine-tuning.md` |
| **1.8** | **PEFT: LoRA & QLoRA Deep Dive** | Low-Rank Adaptation math ($W + B \times A$), rank $r$ vs alpha $\alpha$, 4-bit NormalFloat (NF4) quantization | ⚪ | `01-ai-and-ml/08-lora-qlora-mechanics.md` |
| **1.9** | **Model Alignment: DPO vs RLHF** | Direct Preference Optimization loss function, Bradley-Terry preference model, financial accuracy alignment | ⚪ | `01-ai-and-ml/09-dpo-model-alignment.md` |
| **1.10** | **Inference Serving & Quantization** | vLLM vs Ollama vs llama.cpp, PagedAttention, GGUF/AWQ quantization, continuous batching | ⚪ | `01-ai-and-ml/10-inference-quantization.md` |

---

## Track 2: Advanced Financial RAG & Vector Databases

| # | Topic | Key Deliverable / Concept | Status | Notes Link |
| :---: | :--- | :--- | :---: | :--- |
| **2.1** | **Financial Document Parsing** | Complex PDF structure, extracting multi-page balance sheets, OCR vs native text extractors | ⚪ | `01-ai-and-ml/11-financial-document-parsing.md` |
| **2.2** | **Chunking Strategies for Tables** | Naive vs Semantic vs Table-aware markdown chunking, metadata propagation | ⚪ | `01-ai-and-ml/12-chunking-strategies.md` |
| **2.3** | **Embeddings & Vector Index Math** | Dense embeddings, Cosine vs Dot Product vs Euclidean distance, HNSW index mechanics | ⚪ | `01-ai-and-ml/13-vector-embeddings-hnsw.md` |
| **2.4** | **PostgreSQL + pgvector Integration** | Schema design for financial documents, IVFFlat vs HNSW in pgvector, hybrid filtering | ⚪ | `01-ai-and-ml/14-pgvector-deep-dive.md` |
| **2.5** | **Hybrid Search: Dense + BM25** | Combining semantic similarity with exact keyword matching, Reciprocal Rank Fusion (RRF) | ⚪ | `01-ai-and-ml/15-hybrid-search-rrf.md` |
| **2.6** | **Cross-Encoder Rerankers** | Bi-encoders vs Cross-encoders, BGE/Cohere reranker pipelines, latency vs precision | ⚪ | `01-ai-and-ml/16-rerankers-optimization.md` |
| **2.7** | **Context Engineering & Prompt Caching** | KV-cache prefix reuse, structured JSON schema enforcement (Outlines/Instructor), hallucination guards | ⚪ | `01-ai-and-ml/17-context-engineering.md` |
| **2.8** | **Semantic Caching & Query Expansion** | Redis semantic caching, HyDE (Hypothetical Document Embeddings), query rewriting | ⚪ | `01-ai-and-ml/18-semantic-caching-hyde.md` |
| **2.9** | **RAG Evaluation (RAGAS Framework)** | Faithfulness, Answer Relevance, Context Recall, Context Precision metrics | ⚪ | `01-ai-and-ml/19-rag-evaluation-ragas.md` |
| **2.10** | **Model Context Protocol (MCP)** | Standardizing BSE/NSE live ticker and financial ratio calculators into MCP tool servers | ⚪ | `01-ai-and-ml/20-mcp-server-protocol.md` |

---

## Track 3: Enterprise Microservices with Spring Boot 3 & Java 21

| # | Topic | Key Deliverable / Concept | Status | Notes Link |
| :---: | :--- | :--- | :---: | :--- |
| **3.1** | **Spring Boot 3 & Java 21 Internals** | IoC container lifecycle, Virtual Threads (Project Loom), modern record types | ⚪ | `02-spring-boot-microservices/21-spring-boot-internals.md` |
| **3.2** | **Microservice Architecture Blueprint** | Domain-Driven Design (DDD), bounded contexts, API Gateway pattern | ⚪ | `02-spring-boot-microservices/22-microservice-patterns.md` |
| **3.3** | **Spring Cloud Gateway & Security** | JWT authentication, rate limiting (Redis token bucket), cross-cutting filters | ⚪ | `02-spring-boot-microservices/23-gateway-and-security.md` |
| **3.4** | **Spring Data JPA & Hibernate Performance** | N+1 query problem, L1/L2 cache, projection queries, database migration with Flyway | ⚪ | `02-spring-boot-microservices/24-jpa-performance-flyway.md` |
| **3.5** | **Java-to-Python AI Bridge (gRPC vs REST)** | High-throughput gRPC service definitions with Protocol Buffers, serialization benchmarks | ⚪ | `02-spring-boot-microservices/25-grpc-ai-bridge.md` |
| **3.6** | **Resilience & Fault Tolerance** | Resilience4j circuit breakers, retry policies, fallback degradation mechanisms | ⚪ | `02-spring-boot-microservices/26-resilience4j-fault-tolerance.md` |
| **3.7** | **Distributed Caching with Redis** | Cache-aside pattern, cache stampede prevention, TTL strategies for stock market data | ⚪ | `02-spring-boot-microservices/27-redis-distributed-caching.md` |
| **3.8** | **Event-Driven Architecture (Kafka / RabbitMQ)** | Producer/Consumer patterns, consumer groups, idempotency, event sourcing basics | ⚪ | `02-spring-boot-microservices/28-event-driven-messaging.md` |
| **3.9** | **Automated Pipelines & Quartz Scheduling** | Scheduled jobs for earnings seasons, concurrent task orchestration | ⚪ | `02-spring-boot-microservices/29-quartz-scheduling.md` |
| **3.10** | **Observability: Tracing & Metrics** | OpenTelemetry, Micrometer, Prometheus, distributed tracing across microservices | ⚪ | `02-spring-boot-microservices/30-observability-tracing.md` |

---

## Track 4: Multi-Agent Systems, React Frontend & Integration

| # | Topic | Key Deliverable / Concept | Status | Notes Link |
| :---: | :--- | :--- | :---: | :--- |
| **4.1** | **Multi-Agent Orchestration Patterns** | ReAct pattern, planning agents, reflection loops, multi-agent debate | ⚪ | `01-ai-and-ml/31-multi-agent-patterns.md` |
| **4.2** | **Specialized Financial Agents** | Collector Agent, Forensic Auditor, Valuation Agent, Editor Synthesizer | ⚪ | `01-ai-and-ml/32-specialized-financial-agents.md` |
| **4.3** | **React 18/19 Architecture & Reconciliation** | Fiber architecture, Virtual DOM diffing, concurrent rendering, batching | ⚪ | `03-react-and-frontend/33-react-fiber-reconciliation.md` |
| **4.4** | **Custom Hooks & Modern State Management** | Zustand vs TanStack Query, clean separation of server vs UI state | ⚪ | `03-react-and-frontend/34-state-management-zustand.md` |
| **4.5** | **Streaming Agent Thought Logs (SSE & WebSockets)** | Server-Sent Events architecture, real-time typing effect, handling network disconnects | ⚪ | `03-react-and-frontend/35-sse-websockets-streaming.md` |
| **4.6** | **Interactive Financial Data Visualizations** | Candlestick charts, balance sheet Sankey diagrams, valuation sensitivity tables | ⚪ | `03-react-and-frontend/36-financial-charts-ui.md` |
| **4.7** | **Dynamic Report Builder & PDF Generator** | Markdown rendering with LaTeX formulas ($P/E$, $DCF = \sum \frac{CF_t}{(1+r)^t}$), client-side PDF export | ⚪ | `03-react-and-frontend/37-report-builder-latex-pdf.md` |
| **4.8** | **End-to-End System Integration & Testing** | Contract testing, integration tests across React, Spring Boot, and AI Engine | ⚪ | `02-spring-boot-microservices/38-e2e-integration-testing.md` |
| **4.9** | **Docker Multi-Stage & Cloud Deployment** | Production containerization, Docker Compose full-stack startup, CI/CD pipeline | ⚪ | `02-spring-boot-microservices/39-docker-deployment.md` |
| **4.10** | **Staff-Level System Design & Architecture Review** | End-to-end architecture review, live interview grilling simulation, portfolio defense | ⚪ | `05-interview-vault/40-staff-system-design-defense.md` |
