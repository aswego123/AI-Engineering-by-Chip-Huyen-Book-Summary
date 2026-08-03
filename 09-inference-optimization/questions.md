# ❓ Inference Optimization — Open Questions

## Conceptual
- [ ] Why is decoding memory-bound, not compute-bound?
- [ ] How does PagedAttention actually work?
- [ ] What quality hit does INT4 quantization take on my task?

## Practical
- [ ] What's my p95 TTFT and TPOT?
- [ ] Am I using prompt/prefix caching where possible?
- [ ] Is my batch size tuned for throughput vs latency?
- [ ] Would speculative decoding help my workload?

## Deeper
- [ ] Read *PagedAttention / vLLM* paper.
- [ ] Read *FlashAttention* (v1 + v2).
- [ ] Read *Speculative Decoding* (Leviathan 2022).
- [ ] Benchmark vLLM vs TGI on a 7B model.
