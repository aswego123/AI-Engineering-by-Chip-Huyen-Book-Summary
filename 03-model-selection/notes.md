# 🛒 Model Selection

> Choosing the right foundation model for your specific application.

## Selection Workflow

1. **Filter by hard attributes** (license, size, privacy, data)
2. **Narrow candidates** using public benchmarks
3. **Run your own experiments** with your data
4. **Monitor in production** and collect feedback

## Hard vs. Soft Attributes

| Type | Examples | Can Change? |
|------|----------|-------------|
| **Hard** | License, training data, model size, privacy requirements | ❌ No |
| **Soft** | Accuracy, toxicity, factual consistency | ✅ Yes (via prompting/fine-tuning) |

## Evaluation Criteria (4 Buckets)

1. **Domain-specific capabilities** (does it know your field?)
2. **General capabilities** (coherent, factual, faithful)
3. **Instruction following** (does it follow format requests?)
4. **Cost & latency**

## API vs. Self-Hosted

| Factor | API (OpenAI, etc.) | Self-Hosted (open source) |
|--------|--------------------|--------------------------|
| **Ease** | ✅ Easy start | ❌ Setup required |
| **Privacy** | ❌ Data leaves org | ✅ Full control |
| **Cost at scale** | ❌ Expensive | ✅ Cheaper long-term |
| **Flexibility** | ❌ Limited | ✅ Full customization |
| **Extra features** | ✅ Function calling, guardrails | ❌ Build yourself |

## Terminology Clarified

- **Open source** — weights + training data both public
- **Open weight** — weights public, training data closed (most "open source" models)
- **Proprietary** — everything closed (GPT-4, Claude)

## Benchmarks Warning

- **Data contamination** — model may have seen the test data during training
- Detect via **n-gram overlap** and **unusually low perplexity** on eval data

📖 [Back to book summary](../00-book-overview/summary.md)
