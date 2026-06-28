---
type: concept
title: "Data Science"
address: c-000029
created: 2026-06-28
updated: 2026-06-28
tags:
  - concept
  - data-science
  - field
status: developing
related:
  - "[[Data Science for Beginners]]"
  - "[[Data Science from Scratch]]"
  - "[[From-Scratch Pedagogy]]"
  - "[[Linear Algebra]]"
---

# Data Science

The discipline of extracting knowledge and insight from data. A widely-cited framing (echoed by both vault sources below) places it at the **intersection of three skill sets**:

- **Hacking / programming** — getting, cleaning, and manipulating data in code.
- **Math & statistics** — probability, inference, and the [[Linear Algebra]] underneath models.
- **Substantive / domain expertise** — knowing which questions matter and how to interpret answers.

> [!key-insight] Two routes up the same mountain
> This vault holds the field taught from opposite ends:
> - [[Data Science from Scratch]] (Grus) — **build the algorithms by hand** to understand them ([[From-Scratch Pedagogy]]).
> - [[Data Science for Beginners]] (Microsoft) — **use the libraries and cloud tools** (Pandas, Matplotlib, Azure ML) to ship results, project by project.
> Same Venn diagram, different pedagogy. Beginners often start with the curriculum; the book deepens the math/mechanics.

## The lifecycle (per [[Data Science for Beginners]])

A practical project moves through: **acquisition/extraction → preparation (cleaning) → analysis → communication** — plus the parts pure-ML texts omit: data **ethics**, databases (SQL/NoSQL), visualization, and **cloud deployment**.

## Relationship to ML / deep learning

Data science is the broad umbrella; machine learning is a tool within it. The vault's ML/AI cluster sits downstream:
- foundations: [[Linear Algebra]], statistics, probability
- classical ML: [[Pattern Recognition and Machine Learning]]
- deep learning: [[Deep Learning (Goodfellow, Bengio, Courville)]] → [[Transformer]], [[Modern Large Language Models]]

Data science adds the surrounding craft — data wrangling, visualization, ethics, communication — that turns those models into decisions.
