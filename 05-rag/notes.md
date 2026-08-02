# 📚 RAG (Retrieval Augmented Generation)

> Give the model access to external information it wasn't trained on.

## What is RAG?

Enhances a model's generation by **retrieving relevant info** from external sources (databases, docs, the web) and inserting it into the prompt.

**Two main components:**
1. **Retriever** — fetches relevant info
2. **Generator** — the foundation model using that info

## How Retrieval Works

### Step 1: Indexing
- Split documents into **chunks** (index cards)
- Store chunks in a database or vector store

### Step 2: Querying
- Take user query → find most relevant chunks → add them to the prompt

## Retrieval Methods

### 1. Term-Based (Lexical)
- Match by **keywords** (BM25, TF-IDF)
- ✅ Fast, works with Elasticsearch out of the box
- ❌ Misses semantic relationships

### 2. Embedding-Based (Semantic)
- Convert text → vectors → find **closest meaning**
- Uses **vector databases** (Pinecone, Weaviate, Chroma)
- Uses **approximate nearest neighbors (ANN)** for speed
- ✅ Understands meaning, not just words
- ❌ Bad at exact matches (names, error codes)
- ❌ Expensive to embed

### 3. Hybrid (Production Systems)
- Cheap retriever fetches candidates → precise retriever ranks them

## Chunking Strategy

- **Fixed length** — split by chars/words/sentences/paragraphs
- **Overlapping chunks** — ensures boundary info isn't lost
- Trade-off: smaller = more diverse info but loses context; larger = keeps context but fewer chunks fit

## Enhancements

- **Reranking** — refine initial ranking (by recency, relevance)
- **Query rewriting** — expand ambiguous queries ("What's its population?" → "What's the population of Paris?")
- **Chunk augmentation** — add metadata, tags, summaries

## Multi-Modal & Tabular RAG

- **Multi-modal RAG** — retrieve images alongside text
- **Text-to-SQL** — convert user questions into SQL queries against a database

## Selecting a Vector DB

Consider:
- Retrieval methods supported
- Embedding models & search algorithms
- Scalability, indexing speed, query latency
- Pricing & compliance

📖 [Back to book summary](../00-book-overview/summary.md)
