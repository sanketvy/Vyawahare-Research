# 🎓 Learning Knowledge Base & Interview Goldmine

Welcome to the central repository of first-principles knowledge, architectural decisions, and interview preparation notes for **Vyawahare Research**.

This directory serves two critical purposes:
1. **First-Principles Concept Vault:** Comprehensive, zero-fluff explanations of every topic covered across AI/ML, Java Spring Boot microservices, ReactJS, and Financial Engineering.
2. **Interview Revision & Grilling Sandbox:** Structured so that before any technical interview loop, you can quickly revise any topic, and ask the agent: *"Grill me on Module 2: RAG Architecture"* or *"Conduct a Staff-level System Design interview on our AI Bridge"*.

---

## 📂 Knowledge Base Structure

```text
learning/
├── README.md                          # This orientation guide
├── ROADMAP.md                         # Technical curriculum & concept mastery tracker
├── 01-ai-and-ml/                      # AI foundations, SLMs, Pretraining, RAG, Agents, MCP
│   └── README.md
├── 02-spring-boot-microservices/      # Spring Boot 3, Microservice patterns, gRPC, Kafka
│   └── README.md
├── 03-react-and-frontend/             # React internals, state management, SSE/WebSockets
│   └── README.md
├── 04-financial-engineering/          # Indian markets, valuation math, forensic accounting
│   └── README.md
└── 05-interview-vault/                # Rapid revision flashcards, Q&As, System Design blueprints
    └── README.md
```

---

## 🎯 How We Document Each Concept
For every topic we implement, we create a dedicated note containing:
1. **The Core Intuition & Mathematical Foundations:** What problem does this solve? How does it work under the hood?
2. **Architecture & Trade-off Matrix:** Why did we choose Option A over Option B? (e.g., GQA vs MHA, pgvector vs Qdrant, gRPC vs REST).
3. **Failure Modes & Production Gotchas:** What breaks in production? How do we debug it?
4. **Interview Drill Questions:** 5–10 tough, non-trivial questions (Staff/Senior level) with concise model answers.

---

## ⚡ Interactive Grilling Mode
Whenever you want to test your understanding:
- Tell the agent: *"Grill me on [Topic Name]"* or type `/grill-me`.
- The agent will adopt the persona of a principal engineer/interviewer, asking probing questions, pointing out flaws in your answers, and verifying that you truly understand the concepts from first principles.
