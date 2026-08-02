# 🧠 Foundation Models

> Big pre-trained AI models (like GPT, Claude, Llama) that you build applications on top of.

## Key Concepts

- **Self-supervision** — models learn by predicting missing parts of data (no human labeling needed)
- **LLMs → LMMs** — Large Language Models evolved into Large Multimodal Models (handle text, images, video)
- **Training data problems** — web-crawled data is noisy; ~50% is English; skewed toward tech/business/news
- **Transformer architecture** — uses the **attention mechanism** to process all tokens in parallel

## Transformer Basics

- **Attention mechanism** uses three vectors:
  - **Query (Q)** — what info is the model looking for?
  - **Key (K)** — indices of previous tokens
  - **Value (V)** — actual content of previous tokens
- **Multi-headed attention** — multiple attention heads focus on different token groups
- Two steps: **pre-fill** (process input in parallel) → **decode** (generate one token at a time)

## Scaling Laws

- **Chinchilla scaling law**: training tokens ≈ 20 × model parameters
- Bottlenecks: **running out of quality data** + **electricity constraints** (data centers use 1–2% of global power)

## Post-Training

1. **Supervised Fine-Tuning (SFT)** — teach the model to have conversations, not just complete text
2. **Preference Fine-Tuning** — align with human values (RLHF, DPO)

## Sampling (How Output Is Chosen)

- **Greedy sampling** — always pick most likely token (boring, repetitive)
- **Temperature** — higher = more creative, lower = more deterministic
- **Top-K** — pick from top K most likely tokens
- **Top-P (nucleus)** — pick from smallest set summing to probability P (e.g., 0.9)

📖 [Back to book summary](../00-book-overview/summary.md)
