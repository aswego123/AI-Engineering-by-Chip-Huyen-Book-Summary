# 🍝 Dataset Engineering

> Data is the biggest competitive advantage most companies have. **"Garbage in, garbage out."**

## Model-Centric vs. Data-Centric AI

- **Model-centric** — improve performance by tweaking models (architecture, size)
- **Data-centric** — improve performance by improving data quality
- For companies adapting foundation models, **data-centric wins**

## Data Type by Task

| Task | Data Format |
|------|-------------|
| Self-supervised fine-tuning | Sequences of domain text |
| Instruction fine-tuning | Instruction → response pairs |
| Preference fine-tuning | Instruction → winning response + losing response |
| Reward modeling | Preference data or explicit scores |

## Single-Turn vs. Multi-Turn

- **Single-turn** — one instruction, one response
- **Multi-turn** — full dialogue with clarifications, corrections

## Data Quality Factors

- ✅ **Relevance** — matches your target task
- ✅ **Alignment** — reflects the desired attribute (factual, creative, safe)
- ✅ **Consistency** — annotations agree across examples/annotators
- ✅ **Correct formatting** — follows expected structure
- ✅ **Unique** — minimal duplicates
- ✅ **Compliant** — legal, safe, no PII/toxic content
- ✅ **Coverage** — spans your problem space

## How Much Data?

Depends on:
- **Technique** — full fine-tuning needs orders of magnitude more than PEFT
- **Task complexity** — sentiment classification << medical QA
- **Base model** — stronger model needs less data

**Rule of thumb:**
- **Limited data** → PEFT + strong base model
- **Abundant data** → full fine-tuning on smaller model
- **Start with 50 examples** to test if fine-tuning even helps

## Ways to Get More Data

1. **Data flywheel** — use user interactions to keep improving
2. **Existing datasets** — check licensing and quality
3. **Manual annotation** — invest in **clear guidelines**
4. **Data augmentation** — variants of real data (flipping images, etc.)
5. **Data synthesis** — AI-generated fake data (great for privacy)
6. **Path strategies:**
   - Self-supervised → supervised
   - Adjacent domain → target domain
   - Synthetic → real

## Data Processing Best Practices

- Filter and test on small samples first
- **Never modify data in place** — preserve originals
- Exploratory data analysis (distributions, outliers)
- Check inter-annotator disagreement
- Fact-check and manually inspect examples
- Deduplicate to prevent overrepresentation
- Clean formatting tokens (HTML, markdown)
- Remove PII, toxic content, copyright violations
- Use **active learning** if data > compute budget
- Format for target model (correct tokenizer + chat template)

📖 [Back to book summary](../00-book-overview/summary.md)
