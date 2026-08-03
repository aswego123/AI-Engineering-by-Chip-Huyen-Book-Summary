# 🧪 RAG — Code

## Suggested mini-projects
1. **PDF Q&A** — LangChain or LlamaIndex, `unstructured` parser, Qdrant, reranker.
2. **Hybrid search bench** — dense-only vs BM25-only vs hybrid on your data.
3. **RAGAS eval** — measure faithfulness/relevancy on 100 Q/A pairs.
4. **Contextual retrieval** — implement Anthropic's technique, measure lift.
5. **Agentic RAG** — LangGraph or LlamaIndex agents that decide when to retrieve.

## Stacks worth trying
| Stack | Strength |
|---|---|
| LangChain + Qdrant + Cohere Rerank | Batteries included |
| LlamaIndex + LanceDB | Retrieval-first design |
| Haystack | Production pipelines |
| Vespa | Scale + hybrid built-in |
| `ragatouille` | ColBERT easy mode |

## Setup
```bash
pip install langchain llama-index qdrant-client cohere ragas unstructured
```
