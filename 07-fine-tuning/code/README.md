# 🧪 Fine-Tuning — Code

## Suggested mini-projects
1. **QLoRA on Llama-3.1-8B** — 1k examples of your domain style. Compare to base.
2. **DPO run** — 500 preference pairs. Measure win rate vs SFT-only.
3. **Distill GPT-4 → 7B** — use GPT-4 outputs as SFT data.
4. **Regression suite** — MMLU/GSM8K before + after; make sure no cliff.

## Libraries
- [`unsloth`](https://github.com/unslothai/unsloth) — 2× faster, less VRAM.
- [`axolotl`](https://github.com/axolotl-ai-cloud/axolotl) — YAML-driven, production-y.
- [`trl`](https://github.com/huggingface/trl) — SFTTrainer, DPOTrainer.
- [`peft`](https://github.com/huggingface/peft) — LoRA/QLoRA/DoRA.
- [`distilabel`](https://github.com/argilla-io/distilabel) — synthetic data pipelines.

## Compute
- Local: RTX 4090 handles 7B QLoRA.
- Cloud: RunPod / Modal / Lambda / Together for A100/H100.
