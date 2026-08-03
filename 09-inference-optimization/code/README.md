# 🧪 Inference Optimization — Code

## Suggested mini-projects
1. **Latency bench** — measure TTFT and TPOT for 3 models under load.
2. **Quantization sweep** — FP16 vs INT8 vs INT4 quality vs speed on your eval.
3. **vLLM serving** — deploy Llama-3.1-8B, measure throughput at batch=1/8/32.
4. **Prompt caching demo** — Anthropic prompt caching, measure cost delta.
5. **Semantic cache** — GPTCache in front of your app, measure hit rate + quality.

## Libraries
- [`vllm`](https://github.com/vllm-project/vllm) — high-throughput serving.
- [`sglang`](https://github.com/sgl-project/sglang) — RadixAttention, structured outputs.
- [`llama.cpp`](https://github.com/ggerganov/llama.cpp) — CPU / Metal / edge.
- [`bitsandbytes`](https://github.com/TimDettmers/bitsandbytes) — quantization.
- [`gptcache`](https://github.com/zilliztech/GPTCache) — semantic cache.
- [`locust`](https://locust.io/) / [`k6`](https://k6.io/) — load testing.
