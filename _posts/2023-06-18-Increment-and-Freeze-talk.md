---
layout: post
title: Presentation of Increment-and-Freeze at SPAA
lead: Presented my paper on computing cache hit rate curves at the ACM Symposium on Parallel Algorithms and Architectures.
---

[![](/assets/files/IAFSPAA'23.pdf)](/assets/files/IAFSPAA'23.pdf)

## Symposium on Parallel Algorithms and Architectures (SPAA)
The 35th ACM Symposium on Parallel Algorithms and Architectures (SPAA'23) was held in Orlando Florida on June 17-19th of 2023. I was lucky enough to be able to travel there and present our paper on computing cache hit-rate curves at the conference. SPAA is a venue primarily focused on parallel algorithms theory but also encourages experimental papers and papers that blend both approaches. The community, much like myself, cares about the practical performance of the algorithms it develops.

My talk went well, not necessarily due to the merit of the talk itself, but at least in part because I made everyone laugh at the beginning. My other talks, [including this one](/2022/10/28/GraphZeppelin-at-Graduate-Research-Day), often have humorous elements to keep the audience engaged.

## Topic of Talk
Cache hit-rate curves provide important information to understanding the locality of a program and the trade-off between cache size and program speed. However, computing cache hit rate curves is expensive. The existing algorithms for this computation suffer from a lack of locality incurring O(log) cache misses for each memory access. Thus, these analyses are a log factor slower than the trace itself. This bears out in practice, with hit-rate computation generally being a factor 100x slower than the program which generated the trace.

In this paper, we present a new algorithm Increment-and-Freeze that reduces cache misses and allows for simple parallel computation on stack traces. After these algorithmic improvements and implementation engineering we can perform a computation that takes state of the art algorithms 13 hours in only 12 minutes.

See [the paper](/assets/papers/2023_Increment_and_Freeze.pdf) for more information.

