# 🧪 Evaluation — Code

## Suggested mini-projects
1. **LLM-judge harness** — grade 100 outputs with GPT-4 as judge, compare to your labels.
2. **Bootstrap CIs** — write a function that returns win-rate ± 95% CI.
3. **Bias detector** — swap A/B order; measure position bias in your judge.
4. **Nightly regression** — GitHub Action that runs eval on every PR to prompts.

## Libraries worth knowing
- [`ragas`](https://github.com/explodinggradients/ragas) — RAG evaluation.
- [`deepeval`](https://github.com/confident-ai/deepeval) — pytest-style LLM tests.
- [`promptfoo`](https://www.promptfoo.dev/) — CLI for prompt eval.
- [`inspect_ai`](https://inspect.ai-safety-institute.org.uk/) — UK AISI's eval framework.

## Setup
```bash
pip install ragas deepeval promptfoo openai
```
