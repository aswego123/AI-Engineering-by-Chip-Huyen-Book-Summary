# AI Engineering Overview

## Introduction 🎯

Summary of the book AI Engineering by Chip Win covering key topics in AI.

Focus on foundation models, prompt engineering, RAG, fine-tuning, agents, system building, and optimization.

High-level overview intended as a starting point for further exploration.

## What is AI Engineering? 🤖

### Definition and Growth

AI engineering focuses on building applications on foundation models rather than training from scratch.

Rapid growth due to advances in AI models and lowered barriers to use.

### Foundation Models vs Traditional ML

Foundation models are large pre-trained models using self-supervision.

AI engineers adapt these models instead of developing models end-to-end.

### Applications of Foundation Models

Used in coding assistance, image generation, writing aids, customer support bots, data analysis, etc.

## Foundation Models Deep Dive 📚

### Training Data and Biases

Trained on massive web-crawled data with issues like misinformation and language skew (mostly English).

Specialized models needed for underrepresented languages/domains.

### Transformer Architecture

Replaced older sequence-to-sequence models with attention mechanisms.

Attention enables parallel token processing and focus on relevant input tokens.

Multi-headed attention allows simultaneous focus on diverse token groups.

### Model Scaling and Challenges

Larger models generally perform better but require more compute.

Scaling laws (e.g., Chinchilla) optimize training tokens to model size ratio.

Bottlenecks: data scarcity, energy consumption, and increasingly expensive improvements.

## Model Adaptation Techniques 🔧

### Fine-Tuning

Adjusting model weights to improve domain-specific or task-specific performance.

Parameter-efficient tuning (e.g., LoRA) reduces memory and data requirements.

Techniques include full fine-tuning, partial tuning, adapter-based methods.

### Prompt Engineering

Crafting prompts to direct model output without changing weights.

Components: task description, examples, query.

Techniques include chain-of-thought prompting, persona adoption, output formatting.

Requires experimentation and systematic iteration.

### Retrieval Augmented Generation (RAG)

Combining retrieval of external data with generation to provide updated information.

Retriever indexes and queries external knowledge bases.

Term-based (lexical) and embedding-based (semantic) retrieval methods.

### Agents and Tool Use

Models acting as agents use tools (e.g., web search, SQL queries) for multi-step workflows.

Agents plan, validate, and execute actions sequentially.

Memory systems support information retention across sessions.

## Model Evaluation and Selection 📊

### Challenges

AI tasks are complex, open-ended, and models are black boxes.

Benchmarks saturate quickly; new capabilities must be discovered.

### Metrics

Fundamental: cross-entropy, perplexity, exact match, lexical and semantic similarity.

AI judges (other AI models) are increasingly used for scalable evaluation.

Biases and reproducibility issues exist in metrics.

### Model Selection Criteria

Domain-specific capability, general ability, instruction-following, cost and latency.

Hard attributes (license, privacy) vs. soft attributes (accuracy, toxicity).

Workflow: filter models, benchmark, experiment, monitor continuously.

## Inference Optimization ⚡

### Importance

Real-world usefulness depends on inference speed and cost.

Inference servers run the model for user queries.

### Bottlenecks

Compute-bound (limited by processing power) vs memory bandwidth-bound.

### Performance Metrics

Latency (time to first token, time per token), throughput, and utilization.

### Hardware Considerations

GPUs dominate due to parallelism; choice depends on compute power, bandwidth, and memory size.

### Optimization Techniques

Model compression: quantization, pruning, distillation.

Speculative and parallel decoding to overcome sequential token generation.

Kernel and compiler optimizations.

Service-level optimizations: batching (static, dynamic, continuous), decoupled prefill-decode, caching, parallelism (replica, model, pipeline).

## Building AI Applications 🏗️

### Architecture Evolution

Start simple: query → model → response.

Add context construction via RAG, agents, document upload.

Implement guard rails to protect against failures and attacks.

Introduce model routing and gateways to handle diverse queries.

Optimize with caching and add complex logic (multi-step workflows, write actions).

### Monitoring and Observability

Monitoring detects issues; observability helps diagnose root causes.

Key reliability metrics: MTTD, MTTR, Change Failure Rate.

### Orchestration Tools

Tools like LangChain, LlamaIndex manage pipelines but may add complexity.

Start simple before adopting orchestration layers.

## Data Set Engineering 📂

### Data-Centric AI Approach

Focus on improving data quality over only model architectures.

### Types of Data Needed

Self-supervised sequences, instruction-response pairs, preference data, reward labels.

Need relevance, alignment, consistency, format correctness, diversity, policy compliance.

### Data Volume Considerations

Parameter efficient fine-tuning requires fewer examples than full fine-tuning.

Start with small, well-crafted datasets before scaling up.

### Data Creation Techniques

Data flywheels, available datasets, augmentation, synthetic data generation.

AI-assisted annotation tools improve quality and consistency.

### Data Processing Best Practices

Filtering, exploratory analysis, deduplication, formatting cleaning, compliance checks.

Active learning to optimize data usage under compute constraints.

## Safety and Security in Prompt Engineering 🔐

### Prompt Attacks

Extraction, jailbreaking, injection, and unintended sensitive info disclosure.

### Defense Strategies

Use benchmarks, security red teaming, explicit constraints in prompts.

Guardrails in inputs and outputs.

Anomaly detection and human-in-the-loop checks.

### Balancing Security and UX

Track violation and false refusal rates to maintain smooth user experience.

## Summary and Recommendations 📚

AI engineering requires balancing many components: models, data, evaluation, deployment.

Foundation models enable rapid application development but need adaptation techniques.

Rigorous evaluation and careful model selection are critical.

Optimization at both model and infrastructure levels improves user experience and cost.

Build architectures incrementally, focus on safety and observability.

Data quality and user feedback provide the greatest competitive advantage.

Use this overview as a starting point for deeper study and experimentation.

