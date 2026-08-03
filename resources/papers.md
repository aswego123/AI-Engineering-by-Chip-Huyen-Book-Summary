# 📄 Essential Papers — AI Engineering

> Grouped by chapter. Each entry: **paper — 1-line "why it matters"**.
> Read the abstract + intro + conclusions first. Skim the rest. Come back for details.

---

## 01 — Foundation Models

- **Attention Is All You Need** (Vaswani, 2017) — invents the Transformer, the entire foundation.
- **BERT: Pre-training of Deep Bidirectional Transformers** (Devlin, 2018) — masked LM, encoder-only paradigm.
- **Language Models are Few-Shot Learners** (Brown, 2020, GPT-3) — scale + in-context learning.
- **Training Compute-Optimal Large Language Models** (Hoffmann, 2022, Chinchilla) — the 20 tokens/param rule.
- **LLaMA: Open and Efficient Foundation Language Models** (Touvron, 2023) — the open-model unlock.
- **Scaling Laws for Neural Language Models** (Kaplan, 2020) — original scaling laws.
- **RoFormer: Rotary Position Embedding** (Su, 2021) — RoPE, used by LLaMA/Qwen/etc.
- **GQA: Grouped-Query Attention** (Ainslie, 2023) — inference-friendly attention.
- **Are Emergent Abilities of LLMs a Mirage?** (Schaeffer, 2023) — metric artifacts, not magic.

---

## 02 — Evaluation

- **BLEU: a Method for Automatic Evaluation** (Papineni, 2002) — the reference metric everyone uses and misuses.
- **BERTScore** (Zhang, 2019) — embedding-based similarity.
- **Judging LLM-as-a-Judge with MT-Bench and Chatbot Arena** (Zheng, 2023) — foundational LLM-judge study.
- **G-Eval: NLG Evaluation using GPT-4 with Better Human Alignment** (Liu, 2023) — practical judge design.
- **Chatbot Arena** (Chiang, 2024) — Elo-style human preference evaluation at scale.
- **HELM: Holistic Evaluation of Language Models** (Liang, 2022) — multi-metric benchmark methodology.
- **RAGAS: Automated Evaluation of RAG** (Es, 2023) — the RAG eval framework.

---

## 03 — Model Selection

- **Sparks of Artificial General Intelligence** (Bubeck, 2023) — GPT-4 capability audit; how to probe a model.
- **RouteLLM: Learning to Route LLMs with Preference Data** (Ong, 2024) — cost-aware routing.
- **The False Promise of Imitating Proprietary LLMs** (Gudibande, 2023) — imitation ≠ capability. Careful with distillation claims.

---

## 04 — Prompt Engineering

- **Chain-of-Thought Prompting** (Wei, 2022) — reasoning via prompts.
- **Self-Consistency Improves CoT** (Wang, 2022) — sample many, majority vote.
- **ReAct: Synergizing Reasoning and Acting** (Yao, 2022) — thought-action-observation loop.
- **Tree of Thoughts** (Yao, 2023) — search over reasoning branches.
- **Reflexion: Language Agents with Verbal Reinforcement Learning** (Shinn, 2023) — self-critique.
- **Lost in the Middle** (Liu, 2023) — position bias in long contexts.
- **Large Language Models are Zero-Shot Reasoners** (Kojima, 2022) — "Let's think step by step."
- **DSPy: Compiling Declarative LM Calls** (Khattab, 2023) — programmatic prompt optimization.

---

## 05 — RAG

- **Retrieval-Augmented Generation for Knowledge-Intensive NLP** (Lewis, 2020) — the original RAG paper.
- **Dense Passage Retrieval** (Karpukhin, 2020) — dense retrieval basics.
- **ColBERT: Efficient and Effective Passage Search** (Khattab, 2020) — late interaction retrieval.
- **HyDE: Hypothetical Document Embeddings** (Gao, 2022) — LLM-assisted query.
- **REPLUG: Retrieval-Augmented Black-Box LMs** (Shi, 2023) — retrieval without touching the LM.
- **Self-RAG** (Asai, 2023) — model decides when/what to retrieve.
- **From Local to Global: A GraphRAG Approach** (Edge, Microsoft, 2024) — graph-based RAG.
- **Contextual Retrieval** (Anthropic, 2024, blog) — +49% retrieval with per-chunk context.
- **Corrective RAG (CRAG)** (Yan, 2024) — grade + re-search.

---

## 06 — Agents

- **ReAct** (Yao, 2022) — see 04.
- **Toolformer: LMs Can Teach Themselves to Use Tools** (Schick, 2023) — self-supervised tool use.
- **Voyager: An Open-Ended Embodied Agent with LLMs** (Wang, 2023) — lifelong learning agent.
- **Generative Agents: Interactive Simulacra of Human Behavior** (Park, 2023) — memory + reflection agents.
- **Building Effective Agents** (Anthropic, 2024, blog) — required reading. Patterns > frameworks.
- **SWE-bench: Can LMs Resolve Real-World GitHub Issues?** (Jimenez, 2023) — real agent benchmark.
- **τ-bench: Benchmark for Tool-Agent-User Interaction** (Yao, 2024) — realistic multi-turn tools.

---

## 07 — Fine-Tuning

- **LoRA: Low-Rank Adaptation** (Hu, 2021) — the workhorse of PEFT.
- **QLoRA: Efficient Finetuning of Quantized LLMs** (Dettmers, 2023) — 4-bit + LoRA, laptop-scale.
- **Training Language Models to Follow Instructions with Human Feedback** (Ouyang, 2022, InstructGPT) — RLHF.
- **Direct Preference Optimization** (Rafailov, 2023) — DPO. RLHF without RL.
- **KTO: Model Alignment as Prospect Theoretic Optimization** (Ethayarajh, 2024) — single-thumb feedback.
- **LIMA: Less Is More for Alignment** (Zhou, 2023) — 1k great examples > 100k mid.
- **Textbooks Are All You Need** (Gunasekar, 2023, Phi) — data quality > quantity for pretraining.
- **Constitutional AI** (Bai, Anthropic, 2022) — AI-guided alignment.

---

## 08 — Dataset Engineering

- **The Pile** (Gao, 2020) — early curated pretraining corpus.
- **The RefinedWeb Dataset for Falcon** (Penedo, 2023) — filtered web can match curated.
- **FineWeb** (Penedo, 2024, HF blog + report) — modern web-cleaning pipeline.
- **Deduplicating Training Data Makes LMs Better** (Lee, 2022) — dedup is a free lunch.
- **Self-Instruct: Aligning LMs with Self-Generated Instructions** (Wang, 2022) — synthetic data.
- **Evol-Instruct / WizardLM** (Xu, 2023) — evolve prompts to harder ones.
- **PersonaHub** (Chan, 2024) — 1B personas for diverse synthetic data.

---

## 09 — Inference Optimization

- **FlashAttention** (Dao, 2022) and **FlashAttention-2** (Dao, 2023) — IO-aware attention kernel.
- **Efficient Memory Management for LLM Serving with PagedAttention** (Kwon, 2023, vLLM) — throughput serving.
- **Fast Inference from Transformers via Speculative Decoding** (Leviathan, 2022) — 2-3× speedup.
- **Medusa: Simple LLM Inference Acceleration** (Cai, 2024) — parallel decoding heads.
- **GPTQ / AWQ** (Frantar, 2022 / Lin, 2023) — post-training weight quantization.
- **SmoothQuant** (Xiao, 2022) — activation quantization.
- **Mixtral of Experts** (Jiang, 2024) — production MoE.
- **DeepSeek-V2 / V3** (2024) — MLA attention, MoE efficiency.

---

## 10 — Architecture

- **Designing ML Systems** (Huyen, 2022) — book, not a paper. MLOps foundation.
- **Patterns for Building LLM-Based Systems & Products** (Eugene Yan, 2023, blog) — the reference.
- **Building Effective Agents** (Anthropic, 2024) — see 06.
- **Prompt Injection Attacks Against LLM-Integrated Applications** (Greshake, 2023) — indirect injection.
- **Universal and Transferable Adversarial Attacks on Aligned LMs** (Zou, 2023) — jailbreak research.
- **Llama Guard** (Inan, 2023, Meta) — safety classifier design.

---

## How to read a paper (10-min version)

1. **Title + abstract** — what problem, what result.
2. **Figures + tables** — the actual claims.
3. **Introduction** — motivation and framing.
4. **Conclusion / limitations** — what didn't work.
5. **Skim method** — enough to know if you could reproduce.
6. **Related work** — pointers to the next paper.
7. **Only then, if useful, read details.**
