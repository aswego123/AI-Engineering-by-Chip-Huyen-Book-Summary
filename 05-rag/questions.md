# ❓ RAG — Open Questions

## Conceptual
- [ ] Why does hybrid (dense + BM25) almost always beat either alone?
- [ ] When is GraphRAG worth the complexity?
- [ ] How does contextual retrieval interact with chunking strategy?

## Practical
- [ ] What's my chunk size, overlap, and why?
- [ ] Do I have a reranker? What's the recall lift?
- [ ] Am I enforcing per-user permissions at retrieval time?
- [ ] What's my re-embedding cost when the corpus changes?

## Deeper
- [ ] Read *Lost in the Middle* — implications for top-k ordering.
- [ ] Read Anthropic's *Contextual Retrieval* post.
- [ ] Read Microsoft's *GraphRAG* paper.
- [ ] Try ColBERT via `ragatouille` on your corpus.
