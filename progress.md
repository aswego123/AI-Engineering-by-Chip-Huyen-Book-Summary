# 📈 Progress Tracker

> Check things off as you go. Add dates. Link project code / notes.
> Don't aim for 100% — aim for **one checkbox per week**.

Legend: `[ ]` todo · `[~]` in progress · `[x]` done · _(YYYY-MM-DD)_

---

## 🧭 Meta

- [ ] Read [00-book-overview/summary.md](00-book-overview/summary.md)
- [ ] Skim [glossary.md](glossary.md) once through
- [ ] Star 5 papers from [resources/papers.md](resources/papers.md) to read first
- [ ] Set up Python env + a scratch notebook

---

## 01 — Foundation Models

**Notes**
- [ ] Read [01-foundation-models/notes.md](01-foundation-models/notes.md)
- [ ] Read [01-foundation-models/deep-dive.md](01-foundation-models/deep-dive.md)

**Understand**
- [ ] Attention formula from memory
- [ ] Difference: decoder-only vs encoder-decoder vs encoder-only
- [ ] Tokenization: BPE vs SentencePiece
- [ ] Chinchilla scaling rule
- [ ] Temperature / top-p / top-k intuition

**Do**
- [ ] Token counter script (`tiktoken`)
- [ ] nanoGPT trained on TinyShakespeare
- [ ] Attention viz with `bertviz`
- [ ] Sampling parameter sweep

**Papers**
- [ ] *Attention Is All You Need*
- [ ] *Chinchilla*
- [ ] *LLaMA*

---

## 02 — Evaluation

**Notes**
- [ ] [02-evaluation/notes.md](02-evaluation/notes.md)
- [ ] [02-evaluation/deep-dive.md](02-evaluation/deep-dive.md)

**Understand**
- [ ] Closed vs open-ended eval
- [ ] LLM-judge biases (position, length, self-preference)
- [ ] Bootstrap confidence intervals
- [ ] RAGAS metrics

**Do**
- [ ] LLM-judge harness on 100 examples
- [ ] Bootstrap CI helper function
- [ ] Golden set of 50 examples for your task
- [ ] Nightly regression job

**Papers**
- [ ] *MT-Bench / Chatbot Arena*
- [ ] *G-Eval*
- [ ] *RAGAS*

---

## 03 — Model Selection

**Notes**
- [ ] [03-model-selection/notes.md](03-model-selection/notes.md)
- [ ] [03-model-selection/deep-dive.md](03-model-selection/deep-dive.md)

**Understand**
- [ ] Quality / latency / cost / constraints quadrant
- [ ] Cost math per 1M requests
- [ ] Router pattern (cheap default + expensive fallback)

**Do**
- [ ] Bench 5 models on 50 prompts (CSV)
- [ ] Cost spreadsheet at target volume
- [ ] Router POC via LiteLLM

**Papers**
- [ ] *RouteLLM*

---

## 04 — Prompt Engineering

**Notes**
- [ ] [04-prompt-engineering/notes.md](04-prompt-engineering/notes.md)
- [ ] [04-prompt-engineering/deep-dive.md](04-prompt-engineering/deep-dive.md)

**Understand**
- [ ] Zero-shot → few-shot → CoT → self-consistency ladder
- [ ] Structured outputs (JSON mode, constrained decoding)
- [ ] Prompt injection: direct vs indirect

**Do**
- [ ] Prompt library in git (Jinja templates)
- [ ] CoT vs no-CoT bench on GSM8K subset
- [ ] Structured extraction with `instructor`
- [ ] Try DSPy on one task

**Papers**
- [ ] *Chain-of-Thought*
- [ ] *ReAct*
- [ ] *Lost in the Middle*

---

## 05 — RAG

**Notes**
- [ ] [05-rag/notes.md](05-rag/notes.md)
- [ ] [05-rag/deep-dive.md](05-rag/deep-dive.md)

**Understand**
- [ ] Full pipeline diagram from memory
- [ ] Chunking strategies + trade-offs
- [ ] Hybrid search (dense + BM25 + RRF)
- [ ] Reranker role
- [ ] RAGAS metrics

**Do**
- [ ] PDF Q&A app (LangChain/LlamaIndex + Qdrant)
- [ ] Hybrid vs dense-only ablation on your corpus
- [ ] Reranker lift measurement
- [ ] RAGAS evaluation report
- [ ] Try Contextual Retrieval

**Papers**
- [ ] *RAG (Lewis)*
- [ ] *ColBERT*
- [ ] *GraphRAG*
- [ ] *Contextual Retrieval* (Anthropic)

---

## 06 — Agents

**Notes**
- [ ] [06-agents/notes.md](06-agents/notes.md)
- [ ] [06-agents/deep-dive.md](06-agents/deep-dive.md)

**Understand**
- [ ] Workflow → router → tool-user → autonomous spectrum
- [ ] ReAct vs native function calling
- [ ] Compounding-error math
- [ ] MCP basics

**Do**
- [ ] ReAct from scratch (no framework)
- [ ] Function-calling agent w/ 3 tools
- [ ] LangGraph state machine
- [ ] MCP server exposing one tool
- [ ] Try 5 SWE-bench-lite issues

**Papers**
- [ ] *ReAct*
- [ ] *Reflexion*
- [ ] Anthropic *Building Effective Agents*

---

## 07 — Fine-Tuning

**Notes**
- [ ] [07-fine-tuning/notes.md](07-fine-tuning/notes.md)
- [ ] [07-fine-tuning/deep-dive.md](07-fine-tuning/deep-dive.md)

**Understand**
- [ ] SFT vs preference tuning vs continued pretraining
- [ ] LoRA math (rank, alpha, target modules)
- [ ] QLoRA (4-bit NF4)
- [ ] DPO vs RLHF

**Do**
- [ ] QLoRA on Llama-3.1-8B, 1k examples
- [ ] DPO with 500 preference pairs
- [ ] Regression suite (MMLU/GSM8K) before + after

**Papers**
- [ ] *LoRA*
- [ ] *QLoRA*
- [ ] *DPO*
- [ ] *LIMA*

---

## 08 — Dataset Engineering

**Notes**
- [ ] [08-dataset-engineering/notes.md](08-dataset-engineering/notes.md)
- [ ] [08-dataset-engineering/deep-dive.md](08-dataset-engineering/deep-dive.md)

**Understand**
- [ ] Full lifecycle diagram
- [ ] MinHash / LSH dedup
- [ ] Quality classifier concept
- [ ] Synthetic data risks

**Do**
- [ ] MinHash dedup on 100k docs
- [ ] fastText quality classifier
- [ ] Synthetic Q/A with `distilabel`
- [ ] Argilla annotation session (200 examples)

**Papers**
- [ ] *FineWeb*
- [ ] *Self-Instruct*
- [ ] *LIMA*

---

## 09 — Inference Optimization

**Notes**
- [ ] [09-inference-optimization/notes.md](09-inference-optimization/notes.md)
- [ ] [09-inference-optimization/deep-dive.md](09-inference-optimization/deep-dive.md)

**Understand**
- [ ] TTFT vs TPOT
- [ ] Why decode is memory-bound
- [ ] KV cache + PagedAttention
- [ ] Quantization ladder (FP16 → INT8 → INT4)
- [ ] Speculative decoding

**Do**
- [ ] Latency bench (TTFT, TPOT) for 3 models
- [ ] Quantization sweep on your eval
- [ ] vLLM serving of Llama-3.1-8B
- [ ] Prompt caching cost delta measurement
- [ ] Semantic cache POC

**Papers**
- [ ] *FlashAttention*
- [ ] *PagedAttention / vLLM*
- [ ] *Speculative Decoding*

---

## 10 — Architecture

**Notes**
- [ ] [10-architecture/notes.md](10-architecture/notes.md)
- [ ] [10-architecture/deep-dive.md](10-architecture/deep-dive.md)

**Understand**
- [ ] 9 capabilities checklist
- [ ] Guardrails: input + output
- [ ] Observability what-to-log
- [ ] Deployment: canary, shadow, kill switch

**Do**
- [ ] End-to-end capstone app hitting all 9 capabilities
- [ ] Langfuse / Phoenix instrumentation
- [ ] Red-team session against your app
- [ ] Cost dashboard

**Papers**
- [ ] Eugene Yan *Patterns for LLM Systems*
- [ ] Anthropic *Building Effective Agents*
- [ ] *Prompt Injection Attacks* (Greshake)

---

## 🏁 Milestones

- [ ] Milestone 1 — Finished all notes.md
- [ ] Milestone 2 — Finished all deep-dive.md
- [ ] Milestone 3 — Read 10 papers
- [ ] Milestone 4 — Shipped 3 mini-projects
- [ ] Milestone 5 — Capstone app running
- [ ] Milestone 6 — Blog post / demo / repo published

---

## 📝 Weekly log

<!-- Add one line per week. Newest on top. -->

- _YYYY-MM-DD_ — what I did, what I learned, next.
