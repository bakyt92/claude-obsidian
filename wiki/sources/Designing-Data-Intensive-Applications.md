---
type: source
title: "Designing Data-Intensive Applications"
aliases:
  - "Designing Data-Intensive Applications"
  - "DDIA"
address: c-000030
created: 2026-06-28
updated: 2026-06-28
tags:
  - source
  - distributed-systems
  - databases
  - data-engineering
  - textbook
status: current
source_url: https://0-lucas.github.io/digital-garden/99.-Books/Martin-Kleppmann---Designing-Data-Intensive-Applications_-O%E2%80%99Reilly-Media-(2017).pdf
original_file: ".raw/pdfs/designing-data-intensive-applications.pdf"
raw_file: ".raw/articles/designing-data-intensive-applications-2026-06-28.md"
related:
  - "[[Martin Kleppmann]]"
  - "[[O'Reilly Media]]"
  - "[[Distributed Systems]]"
  - "[[Reliability Scalability Maintainability]]"
---

# Source: Designing Data-Intensive Applications

**Author**: [[Martin Kleppmann]]
**Publisher**: [[O'Reilly Media]], 2017 (1st ed.) · ~590 pp · commonly "DDIA"

> [!key-insight] Principles over products
> "DDIA" is the standard reference for the *ideas* behind data systems — databases, caches, queues, batch and stream processors — taught vendor-neutrally so engineers can reason about tradeoffs rather than memorize one tool. It opens this vault's first **[[Distributed Systems]]** / data-engineering domain, distinct from the ML/data-science cluster but sitting *underneath* it: this is the infrastructure that stores and moves the data that data science analyzes.

## Structure (12 chapters, 3 parts)

| Part | Chapters | Focus |
|------|----------|-------|
| I — Foundations | 1–4 | the three concerns ([[Reliability Scalability Maintainability]]); data models (relational/document/graph); storage engines (LSM-trees, B-trees; OLTP vs OLAP); encoding & schema evolution |
| II — Distributed Data | 5–9 | **replication** (leader/follower, multi-leader, leaderless); **partitioning/sharding**; **transactions** (ACID, isolation); "the trouble with distributed systems" (partial failure, unreliable clocks); **consistency & consensus** (linearizability) |
| III — Derived Data | 10–12 | **batch processing** (MapReduce); **stream processing** (event streams, change data capture); the future of data systems ("unbundling the database") |

See [[Distributed Systems]] for the Part II/III concepts in depth, and [[Reliability Scalability Maintainability]] for the Ch 1 framing.

## Why it matters to this vault

- **Establishes a new domain**: distributed systems & data engineering. Until now the vault's technical depth was ML/AI; DDIA adds the systems layer.
- **The infrastructure under data science**: [[Data Science for Beginners]] teaches *using* SQL/NoSQL databases (lessons 5–6); DDIA explains *how those databases actually work* and how they fail at scale.
- **Resonates with the vault's own design**: the plugin's multi-writer safety (advisory file locks, the v1.7 concurrency model — see [[DragonScale Memory]]) is a tiny instance of the transaction/consistency concerns DDIA Ch 7–9 formalize.

## Notes

- The fetched PDF is an **early-release** copy (~491 pp); Chapter 12 ("The Future of Data Systems") is thin/absent here but present in the final O'Reilly edition.
- Published by [[O'Reilly Media]] (animal cover: a wild boar / "Indian wild boar").
