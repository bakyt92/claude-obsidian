---
type: source
title: "Modern Large Language Models"
aliases:
  - "Modern Large Language Models"
address: c-000014
created: 2026-06-28
updated: 2026-06-28
tags:
  - source
  - llm
  - transformers
  - deep-learning
  - pytorch
  - textbook
status: current
original_file: ".raw/pdfs/modern-large-language-models.pdf"
raw_file: ".raw/articles/modern-large-language-models-2026-06-28.md"
related:
  - "[[Daniel R. Holt]]"
  - "[[PyTorch]]"
  - "[[Transformer]]"
  - "[[Self-Attention]]"
  - "[[Retrieval-Augmented Generation]]"
  - "[[From-Scratch Pedagogy]]"
  - "[[Linear Algebra]]"
  - "[[Deep Learning (Goodfellow, Bengio, Courville)]]"
  - "[[Backpropagation]]"
---

# Source: Modern Large Language Models

**Full title**: *Modern Large Language Models: A First-Principles Guide to Building and Understanding Transformer-Based Language Models*
**Author**: [[Daniel R. Holt]]
**Length**: 721 pages · Dec 2025 · built/read in [[PyTorch]]

> [!key-insight] The thesis
> Understand LLMs by **building one from scratch**. The book works bottom-up — from "a language model is a next-token probability distribution" through implementing [[Self-Attention]] and a full **GPT-mini** in pure [[PyTorch]], training it, aligning it, and deploying it (serving, [[Retrieval-Augmented Generation|RAG]], agents). It is a 2025-era instance of [[From-Scratch Pedagogy]] applied to the [[Transformer]].

## Structure (7 parts, 24 chapters + 7 appendices)

| Part | Chapters | Arc |
|------|----------|-----|
| I — Foundations | 1–4 | what LMs do; vector-space intuition; hands-on math (dot product, cosine, softmax, backprop); tokenization (BPE/SentencePiece) |
| II — Build the transformer | 5–9 | [[Self-Attention]] (Q/K/V, multi-head); the [[Transformer]] block (residuals, layernorm, FFN); GPT architecture (RoPE vs positional); line-by-line attention; **GPT-mini** end-to-end |
| III — Train from scratch | 10–12 | training pipeline (AdamW, batching, checkpointing); pretraining + perplexity; **scaling laws**, depth>width, FLOPs/memory |
| IV — Fine-tune & align | 13–16 | task fine-tuning (catastrophic forgetting); instruction tuning; **RLHF / DPO / ORPO**; **PEFT (LoRA, QLoRA, adapters)** |
| V — Advanced | 17–19 | efficient attention (**FlashAttention, GQA/MQA**, Mamba-style, KV caching); embeddings & vector DBs; quantization (4/8-bit, GPTQ, distillation) |
| VI — Deploy | 20–24 | serving at scale; **RAG from scratch**; autonomous agents (planning, tools, memory); evaluation; safety/alignment |
| VII — Appendices | A–G | PyTorch deep dive, math glossary, troubleshooting, hardware recipes, visual atlas, annotated bibliography, full code listings |

## Why it matters to this vault

- **Closest technical match to the vault's own machinery.** Chapter 21 builds a [[Retrieval-Augmented Generation|RAG]] system from scratch (chunking, indexing, retrieval, eval) — the same problem the vault's `wiki-retrieve` / [[Query-Time Retrieval]] solves. Chapter 18 (embeddings, vector DBs, similarity search) underpins it.
- **Pedagogy twin of [[Data Science from Scratch]]**: same "implement it to understand it" ethos ([[From-Scratch Pedagogy]]), one ML-generation later (transformers/PyTorch instead of classical ML/pure Python).
- **Math grounding** ties straight to [[Linear Algebra]]: embeddings as directions, attention as scaled dot products, similarity as cosine.
- Chapter 22 (agents: planning, tool use, **memory systems**) is conceptual background for this vault's persistent-memory framing ([[Persistent Wiki Artifact]], [[DragonScale Memory]]).

## Notes & caveats

- The PDF is an OceanofPDF aggregator copy (calibre-generated). Treat provenance with mild caution; the technical content is standard and self-consistent with the field.
- This is a 2025 self-published / practitioner title, not a peer-reviewed text — useful as a build guide, not a citation of record. For rigorous theory see [[Pattern Recognition and Machine Learning]].
