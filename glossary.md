# 📖 Glossary — AI Engineering Terms

Quick lookup for beginners. Terms are in **alphabetical order**.

---

**Agent** — AI that can perceive its environment, use tools, and take actions (not just chat).

**Attention Mechanism** — the "engine" inside Transformers that lets the model weigh which input tokens matter most.

**Batching** — grouping multiple requests together to process at once (faster, cheaper).

**Chain of Thought (CoT)** — prompting the model to "think step by step" for better reasoning.

**Chinchilla Scaling Law** — rule of thumb: training tokens ≈ 20 × model parameters.

**Chunking** — splitting long documents into smaller pieces for RAG.

**Context Window** — how much text the model can "see" at once.

**Cross-Entropy** — measures how well a model predicts the next token during training.

**Data Flywheel** — using user interactions to continuously improve the product.

**Distillation** — training a small model to mimic a big model.

**DPO (Direct Preference Optimization)** — newer alternative to RLHF for aligning models.

**Embedding** — a numerical vector representing the meaning of text.

**Fine-Tuning** — further training a pre-trained model on your specific data.

**Foundation Model** — huge pre-trained model (like GPT, Claude) that others build on top of.

**Function Calling** — model outputs structured requests to call external tools/APIs.

**Greedy Sampling** — always pick the most likely next token (boring but predictable).

**Guardrails** — safety filters on input (blocking bad prompts) or output (blocking bad responses).

**Hallucination** — when the AI confidently states something incorrect.

**In-Context Learning** — model learns from examples in the prompt (no retraining).

**Inference** — actually running the model to produce output.

**Jailbreaking** — tricking a model to bypass its safety features.

**KV Cache** — stored key/value vectors from attention, reused to speed up generation.

**Latency** — how long users wait for a response.

**LLM (Large Language Model)** — huge model trained on text (e.g., GPT-4).

**LMM (Large Multimodal Model)** — handles text + images + video.

**LoRA (Low-Rank Adaptation)** — cheap fine-tuning method using small matrices.

**Model Gateway** — unified layer routing between multiple models.

**Model Router** — classifier that decides which model handles a given query.

**MTTD** — Mean Time To Detection (how fast you notice a problem).

**MTTR** — Mean Time To Response (how fast you fix a problem).

**Observability** — enough internal logs to diagnose why something broke.

**Open Weight** — model weights are public, but training data isn't.

**PEFT** — Parameter-Efficient Fine-Tuning (train only a small subset of weights).

**Perplexity** — exponential of cross-entropy; measures model uncertainty.

**Post-Training** — SFT + preference tuning applied after pre-training.

**Prompt Engineering** — writing better instructions to get better outputs.

**Prompt Injection** — attack where user input hijacks the system prompt.

**Quantization** — reducing precision (32-bit → 4-bit) to shrink model size.

**RAG** — Retrieval Augmented Generation; fetch relevant info before generating.

**Reranking** — refining initial retrieval results by another signal (recency, relevance).

**RLHF** — Reinforcement Learning from Human Feedback (aligns model with human preferences).

**Self-Supervision** — model learns by predicting parts of its own input (no labels).

**SFT (Supervised Fine-Tuning)** — teach the model conversation format using instruction data.

**Speculative Decoding** — small draft model + big verifier for faster generation.

**System Prompt** — instructions setting the model's role and constraints.

**Temperature** — sampling parameter; higher = more creative, lower = more focused.

**Throughput** — output tokens per second across all requests.

**Token** — chunk of text the model processes (roughly a word or subword).

**Top-K Sampling** — pick next token from the top K most likely.

**Top-P Sampling** — pick next token from smallest set summing to probability P.

**Transformer** — the neural network architecture behind modern LLMs.

**TTFT** — Time To First Token (latency to see the first output).

**TPOT** — Time Per Output Token (per-token generation speed).

**Vector Database** — stores embeddings for fast semantic search (Pinecone, Chroma, etc.).

📖 [Back to README](README.md)
