# 📝 Evaluation

> How do we know if the AI is actually doing a good job? Harder than it sounds.

## Why Evaluation Is Hard

1. Problems are **inherently complex** (e.g., judging a summary requires reading a whole book)
2. Tasks are **open-ended** (many correct answers)
3. Models are **black boxes**
4. Public benchmarks **saturate quickly**
5. Need to discover **new capabilities**, not just known tasks

## Core Metrics

### For Language Models (Training)
- **Cross-entropy** — how well the model predicts the next token
- **Perplexity** — exponential of cross-entropy; lower = more confident predictions
- Perplexity can also detect if text was in training data (very low) or nonsensical (very high)

### For Applications
- **Functional correctness** — does the system actually do what it should?
- **Exact match** — binary check (e.g., "Who won the Nobel Prize?")
- **Lexical similarity** — token overlap (BLEU, ROUGE, edit distance)
- **Semantic similarity** — meaning overlap using embeddings (cosine similarity)

## AI as a Judge

Use one AI to grade another AI's output.
- ✅ Fast, cheap, no reference data needed
- ✅ Can explain decisions
- ❌ **Biases:** self-bias, position bias, verbosity bias
- ❌ Non-deterministic (different scores on repeat runs)

## Evaluation Pipeline Best Practices

- Test on **different data slices** (avoid Simpson's Paradox)
- Use **bootstrap samples** to check reliability
- Tie metrics to **business impact** (e.g., "90% factual consistency = automate 50% of tickets")
- Combine cheap classifiers (all data) + expensive AI judges (1% sample)

📖 [Back to book summary](../00-book-overview/summary.md)
