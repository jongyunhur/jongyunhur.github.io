---
layout: page
title: Comparing Spinlocks and Ticket Locks on ARMv8
description: A Pthreads benchmark of lock correctness, fairness, and throughput under contention.
period: Oct – Dec 2023
importance: 1
---

In this team project, we implemented a spinlock and a ticket lock using the ARMv8 `LDAXR` and `STLXR` instructions. We used shared-array tests to validate both implementations under multithreaded contention.

We built a Pthreads benchmark to measure runtime and throughput at different thread counts. We then compared how the two locks trade off fairness and scalability as contention increases.
