# 🎙️ The Interview Vault & Grilling Playbook

This playbook defines how to use the notes in this repository to prepare for top-tier technical interviews (Staff / Senior Software Engineer, AI Engineer, Backend Distributed Systems).

---

## 🎯 How to Initiate a Grilling Session with the Agent

Whenever you want to test your command of any concept or module, prompt the agent with one of the following commands:

### Mode 1: Rapid-Fire First-Principles Drill
> *"I just completed Topic [X]. Grill me on [Topic] with 5 challenging, progressive questions. Do not give me the answers—wait for my response after each question and evaluate my depth of understanding."*

### Mode 2: System Design Defense (Senior/Staff Level)
> *"Conduct a 45-minute System Design interview where I must design the [e.g., Financial RAG Pipeline / Java-to-Python AI Bridge / Real-time Agent Streaming Platform]. Ask about trade-offs, bottleneck points, failure scenarios, and latency calculations."*

### Mode 3: "Explain it to a Skeptic"
> *"Act as a skeptical principal engineer who believes [e.g., microservices are unnecessary for this / LoRA loses too much accuracy compared to full fine-tuning]. Challenge my design decisions and force me to defend them with trade-offs and numbers."*

---

## 📑 Core Interview Topics Covered in This Repository

### 1. AI & Machine Learning Engineering
- **Attention Mechanics:** Deriving Self-Attention from first principles; MHA vs MQA vs GQA; KV cache memory formulas ($2 \times b \times s \times h \times l$).
- **Positional Encoding:** Absolute vs Relative vs RoPE (Rotary Position Embeddings); why RoPE preserves relative distances via dot product rotation.
- **PEFT / LoRA:** Rank decomposition matrix math ($W_0 + \frac{\alpha}{r}BA$); gradient flow; why low rank is sufficient for adaptation.
- **RAG Architecture:** Vector indexing algorithms (HNSW graphs, IVFFlat); dense vs sparse (BM25) trade-offs; Reciprocal Rank Fusion (RRF); cross-encoder rerankers.
- **Inference Optimization:** Continuous batching vs static batching; PagedAttention memory fragmentation reduction; AWQ vs GPTQ vs GGUF.

### 2. Java Spring Boot & Microservices
- **Spring Internals:** Inversion of Control (IoC), ApplicationContext, Bean lifecycles, Proxy patterns in `@Transactional`.
- **Java 21 Virtual Threads:** Platform threads vs Virtual Threads (Project Loom); how carrier threads handle blocking I/O; memory footprints.
- **Distributed Systems:** API Gateway routing, Resilience4j Circuit Breaker state transitions (CLOSED, OPEN, HALF-OPEN), Redis distributed locks, Kafka consumer group rebalancing.
- **Inter-service Communication:** gRPC (HTTP/2, multiplexing, Protobuf binary serialization) vs REST (HTTP/1.1, JSON overhead).

### 3. Frontend Architecture (ReactJS)
- **React Internals:** React Fiber reconciliation, work loop, concurrent mode, lane priority scheduling.
- **State & Streaming:** TanStack Query cache invalidation vs Zustand store; Server-Sent Events (SSE) vs WebSockets for unidirectional agent streaming.
