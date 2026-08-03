# 🧪 Model Selection — Code

## Suggested mini-projects
1. **Bench script** — same 50 prompts through 5 models, log quality/latency/cost to CSV.
2. **Cost calculator** — spreadsheet or CLI that takes volume + model → monthly $.
3. **Router POC** — embedding classifier picks cheap vs expensive model.
4. **Contamination check** — grep benchmark strings against your training data.

## Libraries
- [`litellm`](https://github.com/BerriAI/litellm) — one API for many providers.
- [`openrouter`](https://openrouter.ai) — routing + fallbacks.
- [`RouteLLM`](https://github.com/lm-sys/RouteLLM).
