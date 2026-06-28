---
source_url: https://0-lucas.github.io/digital-garden/99.-Books/Martin-Kleppmann---Designing-Data-Intensive-Applications_-O%E2%80%99Reilly-Media-(2017).pdf
pdf_file: .raw/pdfs/designing-data-intensive-applications.pdf
fetched: 2026-06-28
extraction: pypdf (metadata + embedded outline); 491 pages (early-release PDF)
md5: 9e80c0baf0329d6e48497c294f359764
---

# Designing Data-Intensive Applications

**Author**: Martin Kleppmann
**Publisher**: O'Reilly Media, 2017 (1st ed.) · ~590 pages final; this PDF is an early-release (~491pp)

## Premise

A vendor-neutral guide to the principles behind data systems — databases, caches,
queues, stream processors, batch frameworks. Rather than tutorialize one tool, it
extracts the *ideas* (replication, partitioning, transactions, consistency, consensus,
batch/stream processing) and the tradeoffs, so engineers can reason about which tools
fit which problems. Famous for its hand-drawn "tree of contents" maps and clarity.

## Table of Contents (3 parts)

### Part I — Foundations of Data Systems
- Ch 1: Reliable, Scalable and Maintainable Applications (the three core concerns; thinking about data systems)
- Ch 2: Data Models and Query Languages (relational vs document vs graph; declarative query languages)
- Ch 3: Storage and Retrieval (data structures: hash indexes, LSM-trees/SSTables, B-trees; OLTP vs OLAP; column-oriented storage)
- Ch 4: Encoding and Evolution (serialization formats; schema evolution; modes of dataflow)

### Part II — Distributed Data
- Ch 5: Replication (leaders & followers, replication lag, multi-leader, leaderless/quorums)
- Ch 6: Partitioning (sharding key-value data, secondary indexes, rebalancing, request routing)
- Ch 7: Transactions (ACID, weak isolation levels, serializability)
- Ch 8: The Trouble with Distributed Systems (partial failures, unreliable networks, unreliable clocks, knowledge/truth/lies)
- Ch 9: Consistency and Consensus (linearizability, ordering guarantees, distributed transactions, consensus)

### Part III — Derived Data
- Ch 10: Batch Processing (Unix tools, MapReduce & distributed filesystems, beyond MapReduce)
- Ch 11: Stream Processing (event streams, change data capture, processing streams)
- Ch 12: The Future of Data Systems (in the final edition; data integration, "unbundling the database", correctness)

## Notable

- One of the most recommended books for backend / data / platform engineers and system-design interviews.
- Martin Kleppmann is a researcher at the University of Cambridge known for distributed systems, CRDTs, and the "local-first software" movement.
