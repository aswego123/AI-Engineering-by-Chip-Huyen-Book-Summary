# ❓ Foundation Models — Open Questions

> Write questions as you read. Answer them later. Delete when solved.

## Conceptual
- [ ] Why does dividing by $\sqrt{d_k}$ in attention actually help gradients?
- [ ] Why is RoPE better at length extrapolation than sinusoidal encodings?
- [ ] What's the intuition behind "attention heads specialize"? Any evidence?
- [ ] Are "emergent abilities" real or a metric artifact?

## Practical
- [ ] How do I count tokens for a specific model without calling the API?
- [ ] What's the actual context window vs the *effective* context window?
- [ ] When does temperature > 1 make sense?

## Deeper rabbit holes
- [ ] Read Anthropic's *Toy Models of Superposition*.
- [ ] Read *Grokking* (Power et al.) — phase transitions in training.
- [ ] Try nanoGPT and modify one thing (e.g., replace GELU with SiLU).
