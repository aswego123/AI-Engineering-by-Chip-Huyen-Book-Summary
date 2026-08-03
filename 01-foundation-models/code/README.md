# 🧪 Foundation Models — Code

Runnable experiments for this chapter.

## Suggested mini-projects
1. **Token counter** — encode strings with `tiktoken`, compare across models.
2. **Tiny GPT** — clone [nanoGPT](https://github.com/karpathy/nanoGPT), train on TinyShakespeare.
3. **Attention visualizer** — plot attention weights for a sentence using `bertviz`.
4. **Sampling playground** — same prompt, vary temperature / top-p / top-k, compare outputs.

## Suggested layout
```
code/
├── 01_token_counter.py
├── 02_nano_gpt/           # cloned or forked
├── 03_attention_viz.ipynb
└── 04_sampling.py
```

## Setup
```bash
python -m venv .venv && source .venv/bin/activate
pip install tiktoken torch transformers bertviz jupyter
```
