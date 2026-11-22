# 🏗️ Phase 1: Building Our Financial SLM from Scratch

This document defines the step-by-step roadmap to design, build, train, and test our own domain-specific Small Language Model (SLM) for **Vyawahare Research**.

Every stage is grounded in our actual project: understanding the architecture, writing the code, and mastering how each component works in real production systems and technical interviews.

---

## 🗺️ The 6-Stage SLM Lifecycle

```text
┌────────────────────────────────────────────────────────────────────────┐
│                   THE SLM LIFECYCLE FOR OUR PROJECT                    │
└────────────────────────────────────────────────────────────────────────┘

  [ Stage 1: The Blueprint ]
  Understand the 4 core components that make up any SLM:
  Tokenizer ──► Embeddings ──► Transformer Blocks ──► Language Model Head
       │
       ▼
  [ Stage 2: Data Gathering & Curation ]
  Gather real Indian financial text:
  • BSE/NSE filings & quarterly announcements
  • Concall transcripts & annual reports
  • Cleaning raw text and removing noise
       │
       ▼
  [ Stage 3: Tokenization & The Data Loader ]
  How text actually feeds into the model:
  • Building a tokenizer that handles numbers, currency (₹), and financial terms
  • Creating the PyTorch Dataset & DataLoader (inputs and target labels)
       │
       ▼
  [ Stage 4: Assembling the Model Architecture ]
  Coding the model blocks step-by-step:
  • Input Embeddings + Positional Encodings
  • Attention Block (how tokens interact)
  • Feed-Forward Network (how facts and patterns are memorized)
  • Connecting them into one clean SLM class
       │
       ▼
  [ Stage 5: The Pretraining Loop ]
  How the model actually learns:
  • Forward pass ──► Loss calculation (Cross-Entropy) ──► Backprop & Optimizer
  • Tracking training loss to watch the model go from random noise to coherent text
       │
       ▼
  [ Stage 6: Generation & Testing ]
  Prompting our trained SLM to analyze financial statements and generate responses.
```

---

## 📌 Detailed Breakdown of Each Stage

### Stage 1: The Architectural Blueprint
- **Goal:** Understand how the 4 core parts of a language model fit together before writing code.
- **The 4 Parts:**
  1. **Tokenizer:** Translates human characters/words into numerical Token IDs.
  2. **Embedding Layer:** Maps Token IDs to dense coordinate vectors in semantic space.
  3. **Transformer Blocks:** Stacked layers of Self-Attention (communication between tokens) and Feed-Forward Networks (token-level processing).
  4. **Language Model Head:** Linear projection from vector space to vocabulary probabilities to predict the next token.
- **Status:** 🟡 *In Progress*

---

### Stage 2: Data Gathering & Curation (Indian Financial Corpora)
- **Goal:** Build the raw text dataset that our SLM will learn from.
- **Deliverables:**
  - Scraper / collector for BSE/NSE annual reports, quarterly results, and concall transcripts.
  - Data cleaning pipeline: stripping HTML/PDF noise, normalizing currency symbols (`₹`, `Rs`, `Crore`, `Lakh`), and deduplication.
- **Status:** ⚪ *Pending*

---

### Stage 3: Tokenization & The PyTorch Data Loader
- **Goal:** Convert our raw text into model-ready tensor batches.
- **Deliverables:**
  - Training a Byte-Pair Encoding (BPE) tokenizer on our financial corpus.
  - PyTorch `Dataset` and `DataLoader` that split text into chunks of length $T$ and create shifted input/target pairs:
    - Input $x$: `["TCS", "announced", "a", "dividend"]`
    - Target $y$: `["announced", "a", "dividend", "of"]`
- **Status:** ⚪ *Pending*

---

### Stage 4: Assembling the SLM Architecture in Code
- **Goal:** Code the complete neural network architecture step-by-step.
- **Deliverables:**
  - `Embeddings`: Token embeddings + Positional embeddings.
  - `CausalSelfAttention`: Multi-head attention with causal masking.
  - `FeedForward`: MLP layer (Linear $\rightarrow$ GELU/SwiGLU $\rightarrow$ Linear).
  - `TransformerBlock`: LayerNorm $\rightarrow$ Attention $\rightarrow$ Residual $\rightarrow$ LayerNorm $\rightarrow$ FFN $\rightarrow$ Residual.
  - `FinancialSLM`: Top-level model module outputting next-token logits.
- **Status:** ⚪ *Pending*

---

### Stage 5: The Pretraining Loop
- **Goal:** Train the model from scratch on our financial dataset.
- **Deliverables:**
  - Training loop: Forward pass $\rightarrow$ Cross-Entropy Loss $\rightarrow$ Backprop $\rightarrow$ Optimizer step (AdamW).
  - Learning rate schedule with warmup.
  - Loss logging and model checkpoint saving (`.pt`).
- **Status:** ⚪ *Pending*

---

### Stage 6: Generation & Financial Inference
- **Goal:** Generate text from our trained model and evaluate its financial understanding.
- **Deliverables:**
  - Autoregressive text generation function (Temperature, Top-K, Top-P sampling).
  - Testing prompts: *"The Q3 revenue of Infosys grew by..."*
  - Reviewing the model's learned financial representations.
- **Status:** ⚪ *Pending*
