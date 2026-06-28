---
type: concept
title: "Retrieval-Augmented Generation"
address: c-000019
created: 2026-06-28
updated: 2026-06-28
tags:
  - concept
  - llm
  - rag
  - retrieval
status: developing
related:
  - "[[Modern Large Language Models]]"
  - "[[Query-Time Retrieval]]"
  - "[[Wiki vs RAG]]"
  - "[[Transformer]]"
---

# Retrieval-Augmented Generation

**RAG** grounds an LLM's output in external documents fetched at query time, instead of relying only on what the model memorized in its weights. The pattern: **retrieve** relevant chunks → **augment** the prompt with them → **generate** an answer conditioned on that context. It is the standard fix for hallucination and stale knowledge.

> [!key-insight] The pipeline (per [[Modern Large Language Models]], Ch 21)
> 1. **Index**: split a corpus into chunks, embed each into a vector, store in a vector database.
> 2. **Retrieve**: embed the query, find the nearest chunks by similarity (often plus a keyword/BM25 signal).
> 3. **Augment & generate**: paste the retrieved chunks into the prompt; the [[Transformer]] attends over them to produce a grounded answer.
> Quality hinges on **chunking strategy**, embedding quality, and retrieval ranking — and on *evaluating* the retrieval, not just the generation.

## Levers that decide RAG quality

- **Chunking**: size and boundaries of the indexed passages.
- **Hybrid retrieval**: dense (embedding/cosine) + sparse (BM25) signals beat either alone.
- **Reranking / contextual prefixes**: a second pass that reorders or enriches candidates before generation.
- **Evaluation**: measure retrieval hit-rate separately from answer quality (Ch 21, Ch 23).

## Connection to this vault

This vault implements exactly this machinery in miniature:

- [[Query-Time Retrieval]] and the `wiki-retrieve` skill use **contextual prefix + BM25 + cosine rerank** — the same hybrid recipe Ch 21 describes (modeled on Anthropic's Contextual Retrieval research).
- But the vault's [[Wiki vs RAG]] page argues a **curated wiki beats naive RAG** below ~1000 pages: synthesized, human-readable pages outperform dumping raw chunks into a vector DB. The resolution: RAG is the *retrieval technique*; the wiki is a *curation discipline layered on top of it*. They are not opposites so much as different altitudes — see [[Wiki vs RAG]] for the tradeoff.

> [!note] Not a contradiction
> [[Modern Large Language Models]] treats RAG as the default grounding pattern; [[Wiki vs RAG]] is skeptical of *naive* RAG at small scale. Both can hold: use retrieval, but curate what you retrieve over.
