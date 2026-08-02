# 🏎️ Inference Optimization

> Making models **fast** and **cheap** to run in production.

## Training vs. Inference

- **Training** — build the model
- **Inference** — use the model to compute outputs
- **Inference server** — hosts the model, runs it, returns responses

## Bottleneck Types

| Bottleneck | Cause | Example |
|------------|-------|---------|
| **Compute-bound** | Not enough processing power | Image generation |
| **Memory bandwidth-bound** | Data movement between memory ↔ processor | LLM autoregressive inference |

Use **NVIDIA Nsight** and **roofline charts** to identify.

## Inference API Types

- **Online API** — optimizes for latency (chatbots)
- **Batch API** — optimizes for cost (reports, synthetic data)

## Key Metrics

### Latency
- **TTFT** — Time To First Token
- **TPOT** — Time Per Output Token
- **Total latency** = TTFT + TPOT × output tokens
- **TTP** — Time To Publish (may differ if AI plans before responding)
- Use **percentiles** (p50, p95, p99), not averages

### Throughput
- Output tokens per second across all requests
- Higher throughput = lower cost
- ⚠️ Latency-throughput trade-off

### Utilization
- **MFU** — Model FLOPs Utilization
- **MBU** — Model Bandwidth Utilization

## Hardware

| Type | Cores | Best For |
|------|-------|----------|
| **CPU** | Few powerful cores | General computing |
| **GPU** | Thousands of small cores | Parallel matrix math (ML) |

Focus on: **FLOPS**, **memory size**, **memory bandwidth**.

## Model-Level Optimizations

### Model Compression
- **Quantization** — reduce precision (most popular)
- **Pruning** — remove less important weights
- **Distillation** — small model mimics large one

### Autoregressive Speedups
- **Speculative decoding** — small draft model + big verifier
- **Reference copies** — reuse input tokens when possible
- **Parallel decoding** — generate multiple tokens at once
- **Attention optimization** — FlashAttention, etc.

### Kernels & Compilers
- **Kernels** — hand-tuned code for specific hardware
- **Compilers** — convert models → optimized code (TensorRT, XLA)
- Techniques: vectorization, parallelization, loop tiling, operator fusion

## Service-Level Optimizations

### Batching Strategies

| Type | Description | Trade-off |
|------|-------------|-----------|
| **Static** | Wait for fixed batch size | Inconsistent latency |
| **Dynamic** | Fill batch OR wait max time | More consistent |
| **Continuous** | Return responses as ready, add new requests | Best UX, complex to build |

### Other Techniques
- **Decoupled prefill/decode** — separate the two phases for efficiency
- **Prompt caching** — save common overlapping segments (system prompts, docs)

## Parallelism

### Replica Parallelism
- Multiple copies of the model, each handling different requests
- Simple, great for high throughput

### Model Parallelism
- **Tensor parallelism** — split operations
- **Pipeline parallelism** — split into sequential stages
- **Context parallelism** — split input sequences
- **Sequence parallelism** — split operations across machines

## What Actually Matters?

Most impactful techniques for typical apps:
1. **Quantization**
2. **Tensor parallelism**
3. **Replica parallelism**
4. **Attention mechanism optimization**

📖 [Back to book summary](../00-book-overview/summary.md)
