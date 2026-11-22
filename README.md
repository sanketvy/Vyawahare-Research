# Vyawahare Research

> This repository contains the implementation of **Vyawahare Research**, an automated equity research platform which can help evaluate, analyze, and generate institutional-grade research reports for Indian stock market companies (NSE & BSE).

---

## 🎯 Primary Mission & Philosophy

The primary objective of this project is **first-principles learning and mastery** across the entire modern AI engineering spectrum, microservices architecture with **Java Spring Boot**, and modern frontend design with **ReactJS**. 

The equity research platform serves as the real-world sandbox and by-product of this journey.

---

## 🧠 Core Exploration & Tech Stack

### 1. AI & Machine Learning Engineering
- **Architectures & SLMs:** Transformer foundations, tokenization (financial BPE), attention variants (MHA, GQA, FlashAttention), and domain-specific Small Language Models.
- **Pretraining & Continued Pretraining:** Ingesting and training models on Indian financial corpora (SEBI filings, concall transcripts, annual reports).
- **Fine-Tuning & Alignment:** SFT (Supervised Fine-Tuning), PEFT (LoRA, QLoRA), and DPO/RLHF for financial summarization and reasoning.
- **Inference Engineering:** Serving with vLLM/Ollama, quantization (AWQ, GPTQ, GGUF), KV-cache optimization, and continuous batching.
- **Context Engineering & RAG:** Table-aware chunking, dense + sparse (BM25) hybrid retrieval, reranking, and semantic caching.
- **Multi-Agent Systems & MCP:** Autonomous collaborative research agents (Data Collector, Financial Analyst, Forensic Auditor, Report Synthesizer) with standardized Model Context Protocol (MCP) tool integration.

### 2. Enterprise Backend (Java Spring Boot)
- **Spring Boot 3.x:** Dependency Injection, Spring Security, Spring Data JPA.
- **Microservices:** API Gateway, service discovery, inter-service communication (REST, gRPC, event-driven with Kafka).
- **Python-Java Bridge:** High-throughput RPC/REST integration between Spring Boot services and Python AI inference engines.
- **Resilience:** Circuit breakers (Resilience4j), distributed caching (Redis), and automated earnings calendar schedulers.

### 3. Frontend (ReactJS)
- **Financial Visualizations:** Interactive stock charts, balance sheet tree views, and financial ratios dashboards.
- **Interactive Reports:** Dynamic report builder with LaTeX financial math support and PDF export.
- **Real-Time Agent Streams:** Server-Sent Events (SSE) / WebSockets for streaming agent reasoning logs and reports.

---

## 📂 Target Project Layout

```text
vyawahare-research/
├── GEMINI.md                    # Persistent agent context & learning roadmap
├── AGENTS.md -> GEMINI.md       # Symlink for agent compatibility
├── agent.md -> GEMINI.md        # Symlink for agent compatibility
├── ai-engine/                   # AI/ML pipelines
│   ├── models/                  # SLM architectures, pretraining & fine-tuning
│   ├── inference/               # Serving (vLLM, Ollama), quantization
│   ├── rag/                     # Parsers, chunkers, vector DB connectors
│   ├── agents/                  # Multi-agent workflows & orchestration
│   └── mcp/                     # MCP servers & financial scrapers
├── backend/                     # Java Spring Boot microservices
│   ├── api-gateway/             # Gateway service
│   ├── research-service/        # Core business logic
│   └── ai-bridge-service/       # gRPC/REST bridge to Python AI services
├── frontend/                    # ReactJS application
├── data/                        # Corpora, filings, scrapers
└── deployment/                  # Docker, Compose, Kubernetes, CI/CD
```

---

## 🚀 Getting Started

*(Detailed setup instructions for the Python AI engine, Spring Boot microservices, and React frontend will be documented as each module is built.)*

---

## 📜 License
MIT License.
