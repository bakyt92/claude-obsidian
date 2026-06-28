---
type: concept
title: "Distributed Systems"
address: c-000032
created: 2026-06-28
updated: 2026-06-28
tags:
  - concept
  - distributed-systems
  - databases
  - data-engineering
status: developing
related:
  - "[[Designing Data-Intensive Applications]]"
  - "[[Martin Kleppmann]]"
  - "[[Reliability Scalability Maintainability]]"
  - "[[DragonScale Memory]]"
---

# Distributed Systems

Systems whose data and computation are spread across **multiple machines** that communicate over a network. You go distributed to get scale, fault tolerance, and lower latency — and in exchange you inherit a hard new class of problems. The domain hub for the vault's data-engineering cluster, anchored by [[Designing Data-Intensive Applications]].

> [!key-insight] The trouble with distributed systems
> The defining difficulty (DDIA Ch 8) is **partial failure**: some nodes work while others fail or become unreachable, and you often *cannot tell which*. Networks drop and delay messages arbitrarily; clocks drift; a node may be alive but slow. Almost every distributed-systems idea is a strategy for staying correct and available despite this uncertainty.

## The core building blocks (DDIA Part II)

| Idea | What it buys | The catch |
|------|-------------|-----------|
| **Replication** | fault tolerance, read scaling | keeping copies consistent (replication lag, conflicts) |
| **Partitioning / sharding** | write & storage scaling | routing, rebalancing, cross-partition queries |
| **Transactions** | all-or-nothing correctness (ACID) | weak isolation levels have subtle anomalies |
| **Consensus** (e.g. Raft/Paxos) | agreement despite failures | linearizability is expensive; CAP-style tradeoffs |

## Derived data (DDIA Part III)

- **Batch processing** (MapReduce and successors): high-throughput jobs over bounded datasets.
- **Stream processing**: continuous processing of unbounded event streams; change data capture turns a database's writes into a stream.

## Connection to this vault

> [!note] The vault is a tiny distributed-data problem
> claude-obsidian's v1.7 **multi-writer safety** — advisory file locks so two agents don't trample the same page — is a miniature version of the transaction/consistency concerns above (DDIA Ch 7–9). The vault chose pessimistic locking; DDIA surveys the full menu (optimistic concurrency, MVCC, consensus). See [[DragonScale Memory]].
