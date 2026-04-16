## PhysMaster

### Basic Info

PhysMaster is an autonomous AI physicist designed for end-to-end theoretical and computational physics research, integrating rigorous analytical reasoning with executable numerical computation.

📄 Technical Report v1: https://arxiv.org/abs/2512.19799

### ⚙️ Technical Highlights

- **Flexible subtask decomposition and scheduling**  
  Dynamically decomposes complex research problems into structured subtasks with adaptive execution.

- **MCTS-driven balanced exploration**  
  Leverages Monte Carlo Tree Search to balance exploration and exploitation in long-horizon reasoning.

- **Hierarchical academic knowledge base for enhanced reliability**  
  Improves decision-making via structured priors, curated literature, and validated methodology traces.

---

### 🔓 Open Source (Planned before May 2026)

The new version of PhysMaster will introduce:

- Full compatibility with skill ecosystems
- More efficient context management and memory
- Pre-built physics prior knowledge base
- High-precision RAG (Retrieval-Augmented Generation)
- Improved visualization

---

## PRL-Bench: A Benchmark of Physics Research by LLMs

### Overview

PRL-Bench (Physics Research by LLMs) is a research-oriented benchmark for evaluating large language models on end-to-end physics research tasks, with emphasis on exploration, long-horizon reasoning, and verifiable workflows.

---

### 🧩 Key Characteristics

- **Source**  
  Constructed from 100 authoritative papers from _Physical Review Letters (PRL)_ (Aug 2025 – Mar 2026)

- **Subfield Coverage**
  - Astrophysics (Astro)
  - Condensed Matter (Cond-Mat)
  - High-Energy Physics (HEP)
  - Quantum Information (Quantum)
  - Statistical Physics (Stat)

- Exploration-oriented (implicit solution paths) and long-horizon task with verifiable outputs

- Structure of Task：Research Motivation, Subtasks, Answers & Rubrics and Detailed solution

---

### 📈 Evaluation

We evaluate frontier LLMs under a unified setting with tool access for code execution. Each task is independently run multiple times, and results are averaged and normalized to a 0–100 scale.

| Model               | Astro | Cond-Mat |   HEP | Quantum |  Stat | Global |
| ------------------- | ----: | -------: | ----: | ------: | ----: | -----: |
| GPT-5.4             | 35.02 |    37.49 | 30.99 |   40.37 | 33.88 |  37.38 |
| Gemini-3.1-Pro      | 37.41 |    43.74 | 47.52 |   47.64 | 40.76 |  44.27 |
| Claude-Opus-4.6     | 28.75 |    39.36 | 40.46 |   39.98 | 32.10 |  37.40 |
| Doubao-Seed-2.0-Pro | 28.76 |    40.49 | 35.55 |   42.67 | 24.94 |  37.83 |
| Qwen-3.5-Plus       | 34.51 |    42.82 | 37.16 |   43.72 | 25.87 |  40.05 |
| Kimi-K2.5           | 27.86 |    34.42 | 31.82 |   38.16 | 25.71 |  33.89 |

> Average performance of state-of-the-art LLMs on PRL-Bench.

---

### 🔍 Findings

- Frontier models achieve **<50 average score** (best ≈ 44.27), indicating that end-to-end research-oriented physics tasks remain highly challenging.

- Failures are dominated by:
  - **Conceptual / formulaic errors**  
    Inappropriate theoretical models or formulas, misuse of physical assumptions, and reliance on superficially relevant but incorrect templates, indicating insufficient mastery of frontier-level physics knowledge.

  - **Unstable long-horizon reasoning**  
    Derivation chains often become inconsistent or break under extended reasoning, with unsupported intermediate steps and difficulty maintaining coherent trajectories, limiting completion of full research workflows.

---

### 🤗 Data

- Hugging Face: https://huggingface.co/datasets/AdrianMiao/PRL_Bench
