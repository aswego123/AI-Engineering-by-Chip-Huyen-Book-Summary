# 🧪 Architecture — Code

## Capstone mini-project
Build one small end-to-end app touching **every** capability:
- FastAPI gateway with auth + rate limit.
- Input guardrail (PII + injection).
- Router (small model default, big on complexity signal).
- RAG (Qdrant + hybrid + reranker).
- One MCP tool.
- LiteLLM abstraction over 2 providers.
- Langfuse tracing.
- Nightly eval job (promptfoo or deepeval).
- Prompt versioned in git; canary deploy via feature flag.

## Libraries
- [`fastapi`](https://fastapi.tiangolo.com/), [`litellm`](https://github.com/BerriAI/litellm), [`langfuse`](https://langfuse.com/), [`qdrant-client`](https://qdrant.tech/), [`presidio`](https://github.com/microsoft/presidio), [`llamaguard`](https://huggingface.co/meta-llama/LlamaGuard-7b), [`promptfoo`](https://www.promptfoo.dev/).

## Layout
```
code/
├── app/
│   ├── gateway.py
│   ├── guardrails.py
│   ├── router.py
│   ├── rag/
│   ├── tools/
│   └── main.py
├── prompts/          # versioned Jinja templates
├── evals/            # golden set + scripts
└── deploy/           # Docker + CI
```
