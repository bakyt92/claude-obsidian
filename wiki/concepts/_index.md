---
type: meta
title: "Concepts Index"
updated: 2026-04-07
tags:
  - meta
  - index
  - concept
domain: knowledge-management
status: evergreen
related:
  - "[[index]]"
  - "[[dashboard]]"
  - "[[Wiki Map]]"
  - "[[Hot Cache]]"
  - "[[LLM Wiki Pattern]]"
  - "[[Compounding Knowledge]]"
  - "[[LLM Wiki Pattern]]"
  - "[[Hot Cache]]"
  - "[[Compounding Knowledge]]"
---

# Concepts Index

Navigation: [[index]] | [[entities/_index|Entities]] | [[sources/_index|Sources]]

All concept pages — ideas, patterns, and frameworks extracted from sources.

---

## Knowledge Management

- [[LLM Wiki Pattern]] — the core architecture for persistent, compounding knowledge bases
- [[Hot Cache]] — ~500-word session context file, updated after every ingest
- [[Compounding Knowledge]] — why the wiki grows more valuable over time, unlike RAG
- [[DragonScale Memory]] — memory-layer spec: fold operator, deterministic page addresses, semantic tiling, boundary-first autoresearch (status: shipped v0.4, all four mechanisms opt-in)
- [[Persistent Wiki Artifact]]: durable Markdown page as the LLM's memory object (developing)
- [[Source-First Synthesis]]: provenance discipline for LLM wiki layers (developing)
- [[Query-Time Retrieval]]: query synthesis with citations, complementary to Obsidian search (developing)

---

## Mathematics

- [[Linear Algebra]] — vector spaces and linear maps; the factorization-centric view (LU/QR/SΛS⁻¹/SVD) and the substrate of modern ML
- [[Four Fundamental Subspaces]] — Strang's "big picture": column/row space, null/left-null space and their orthogonality

---

## Pedagogy

- [[From-Scratch Pedagogy]] — learn a tool by building it by hand before reaching for a library; the philosophy *Data Science from Scratch* embodies

---

## LLMs & Deep Learning

- [[Transformer]] — the attention-based architecture under modern LLMs; a stack of self-attention + FFN blocks
- [[Self-Attention]] — Query/Key/Value mechanism; each token attends to all others via scaled dot products
- [[Retrieval-Augmented Generation]] — RAG: retrieve external chunks, augment the prompt, generate; the technique behind `wiki-retrieve`

---

## Add new concepts here as they are extracted from sources.
