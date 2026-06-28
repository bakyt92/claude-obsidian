---
type: concept
title: "Transformer"
address: c-000017
created: 2026-06-28
updated: 2026-06-28
tags:
  - concept
  - llm
  - deep-learning
  - architecture
status: developing
related:
  - "[[Self-Attention]]"
  - "[[Modern Large Language Models]]"
  - "[[PyTorch]]"
  - "[[Linear Algebra]]"
---

# Transformer

The neural-network architecture underlying modern LLMs. Introduced in the 2017 paper *"Attention Is All You Need,"* it replaced recurrence with [[Self-Attention]], making sequence models **fully parallelizable** over positions and enabling the scale that produced GPT, LLaMA, and Mistral.

> [!key-insight] One block, stacked N times
> A decoder-only ("GPT") transformer is just a stack of identical blocks. Each block is: **[[Self-Attention|multi-head self-attention]] → add residual → layer-norm → feed-forward network → add residual → layer-norm.** Tokens enter as embeddings plus positional information; after N blocks, a linear "language-modeling head" projects the final vectors back to a probability distribution over the vocabulary. That distribution *is* the model's next-token prediction.

## The pieces (per [[Modern Large Language Models]], Part II)

| Component | Role |
|-----------|------|
| Token + positional embeddings | turn token IDs into vectors; inject order (learned positions or **RoPE**) |
| [[Self-Attention]] (multi-head) | mix information across positions |
| Residual connections | preserve gradient flow through deep stacks |
| Layer normalization | stabilize activations |
| Feed-forward network (MLP) | per-position nonlinear transformation |
| LM head | project to vocabulary logits → softmax |

## Why it matters

- **Parallelism**: unlike RNNs, all positions are processed at once — the property that made large-scale pretraining feasible.
- **Depth over width**: [[Modern Large Language Models]] (Ch 12) argues depth (more blocks) buys more than width, a key scaling-law intuition.
- **Modern variants** trade quadratic attention cost for efficiency: FlashAttention, grouped/multi-query attention (GQA/MQA), and recurrent (Mamba-style) alternatives.

## Grounding

The whole architecture is linear-algebra-in-motion: embeddings are vectors, attention is scaled dot products, the FFN is matrix multiplies. See [[Linear Algebra]]. Built from scratch in [[PyTorch]] in the source book.
