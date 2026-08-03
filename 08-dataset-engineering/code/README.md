# 🧪 Dataset Engineering — Code

## Suggested mini-projects
1. **Dedup pipeline** — MinHash + LSH on 100k documents.
2. **Quality classifier** — train fastText on curated vs random web.
3. **Synthetic Q/A generator** — seed docs → questions with `distilabel`.
4. **PII scrubber** — regex + spaCy NER, benchmark false positives.
5. **Annotation UI** — spin up Argilla, label 200 examples.

## Libraries
- [`datatrove`](https://github.com/huggingface/datatrove) — pipeline for large-scale text processing.
- [`datasketch`](https://github.com/ekzhu/datasketch) — MinHash / LSH.
- [`distilabel`](https://github.com/argilla-io/distilabel) — synthetic data.
- [`argilla`](https://github.com/argilla-io/argilla) — annotation platform.
- [`presidio`](https://github.com/microsoft/presidio) — PII detection.
- [`fasttext`](https://fasttext.cc/) — quality/langid classifiers.
