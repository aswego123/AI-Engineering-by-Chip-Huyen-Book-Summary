# 📚 AI Engineering — Study Notes

Personal study notes based on the book **"AI Engineering" by Chip Huyen**.

> Goal: Learn AI Engineering from scratch (beginner-friendly), organized topic by topic.

---

## 📂 Folder Structure

```
ai-engineering/
├── README.md                          ← You are here (index)
├── 00-book-overview/                  ← Book summary & big picture
│   └── summary.md
├── 01-foundation-models/              ← What are LLMs, Transformers, etc.
│   └── notes.md
├── 02-evaluation/                     ← How to grade AI outputs
│   └── notes.md
├── 03-model-selection/                ← Picking the right model
│   └── notes.md
├── 04-prompt-engineering/             ← Talking to AI effectively
│   └── notes.md
├── 05-rag/                            ← Retrieval Augmented Generation
│   └── notes.md
├── 06-agents/                         ← AI with tools & planning
│   └── notes.md
├── 07-fine-tuning/                    ← Customizing models
│   └── notes.md
├── 08-dataset-engineering/            ← Data quality & preparation
│   └── notes.md
├── 09-inference-optimization/         ← Speed & cost
│   └── notes.md
├── 10-architecture/                   ← Putting it all together
│   └── notes.md
├── resources/                         ← Extra learning material
│   └── links.md
└── glossary.md                        ← Quick term lookup
```

---

## 🗺️ Learning Path (Recommended Order)

| # | Topic | Why |
|---|-------|-----|
| 1 | [Book Overview](00-book-overview/summary.md) | Big picture first |
| 2 | [Foundation Models](01-foundation-models/notes.md) | Understand the "brain" |
| 3 | [Prompt Engineering](04-prompt-engineering/notes.md) | Easiest, hands-on start |
| 4 | [Evaluation](02-evaluation/notes.md) | How to know it works |
| 5 | [RAG](05-rag/notes.md) | Give AI your own docs |
| 6 | [Agents](06-agents/notes.md) | AI that takes actions |
| 7 | [Fine-Tuning](07-fine-tuning/notes.md) | Deep customization |
| 8 | [Dataset Engineering](08-dataset-engineering/notes.md) | Data = secret sauce |
| 9 | [Model Selection](03-model-selection/notes.md) | Choose wisely |
| 10 | [Inference Optimization](09-inference-optimization/notes.md) | Make it fast/cheap |
| 11 | [Architecture](10-architecture/notes.md) | Ship a real app |

---

## 🎯 Quick Reference

- **New to AI?** Start with [00-book-overview/summary.md](00-book-overview/summary.md)
- **Confused by a term?** Check [glossary.md](glossary.md)
- **Want more resources?** See [resources/links.md](resources/links.md)
- **Papers to read?** See [resources/papers.md](resources/papers.md)
- **Track your learning:** [progress.md](progress.md)

---

## 🔬 Going Deeper

Each chapter folder now has three tiers:

| File | Purpose |
|---|---|
| `notes.md` | Beginner-friendly overview (start here) |
| `deep-dive.md` | Math, mechanisms, patterns, diagrams |
| `questions.md` | Open questions you're wrestling with |
| `code/` | Runnable mini-projects |

Recommended flow per chapter:
1. Read `notes.md` (30 min)
2. Read `deep-dive.md` (60 min)
3. Pick **one** mini-project from `code/README.md` and ship it
4. Read **one** paper from `resources/papers.md`
5. Check off items in [progress.md](progress.md)
