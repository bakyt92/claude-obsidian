---
type: concept
title: "Reliability, Scalability, Maintainability"
aliases:
  - "Reliability Scalability Maintainability"
  - "Reliability, Scalability, Maintainability"
address: c-000033
created: 2026-06-28
updated: 2026-06-28
tags:
  - concept
  - distributed-systems
  - software-architecture
status: developing
related:
  - "[[Designing Data-Intensive Applications]]"
  - "[[Distributed Systems]]"
---

# Reliability, Scalability, Maintainability

The three concerns [[Designing Data-Intensive Applications]] (Ch 1) names as the goals every data system is judged against. They are the vocabulary the rest of the book uses to evaluate tradeoffs.

> [!key-insight] What each one means (Kleppmann's framing)
> - **Reliability** — the system keeps working *correctly* even when things go wrong (hardware faults, software bugs, human error). Fault-tolerance is engineered by *expecting* faults: redundancy, testing, and deliberately injecting failures.
> - **Scalability** — the system can cope with *growth* in load. The key is to describe load and performance with concrete numbers (e.g. request throughput, p95/p99 latency percentiles — not averages) before reasoning about how to handle 10× the load.
> - **Maintainability** — people can *work on* the system productively over time. Three sub-goals: **operability** (easy to run), **simplicity** (manage complexity; avoid accidental complexity), and **evolvability** (easy to change).

## Why it's the book's spine

Almost every later chapter is an answer to "how does choice X affect reliability, scalability, or maintainability?" Replication and partitioning serve scalability and reliability; transactions and consensus serve reliability (correctness); good data models and encoding serve maintainability (evolvability).

## Beyond data systems

The triad travels well: it is a useful checklist for evaluating *any* software architecture — including, loosely, this vault's own design choices (the v1.7 locking model trades a little simplicity for reliability under concurrent writes). See [[Distributed Systems]].
