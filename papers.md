---
layout: page
title: Publication List
---

# My Publications

## Don't Melt Your Cache: Low-Associativity with Heat-Sink
[Download Paper](/assets/papers/2025_low_assoc_heat_sink.pdf)

Michael A. Bender, Alex Conway, Daniel DeLayo, Martin Farach-Colton, Jaehyun Han, Linfeng He, Rob Johnson, Sudarsun Kannan, William Kuszmaul, Donald Porter, **Evan West**. 2025. Don’t Melt Your Cache: Low-Associativity with Heat-Sink. In *37th ACM Symposium on Parallelism in Algorithms and Architectures (SPAA ’25)*, July 28–August 1, 2025, Portland, OR, USA. ACM, New York, NY, USA, 11 pages. [https://doi.org/10.1145/3694906.3743303](https://doi.org/10.1145/3694906.3743303)

<details>
<summary>Abstract</summary>
Perhaps the most influential result in the theory of caches is the following theorem due to Sleator and Tarjan: With 𝑂(1)resource augmentation, the basic LRU eviction policy is guaranteed to be 𝑂(1)-competitive with the optimal offline policy. 
<br><br>
Sleator and Tarjan’s result applies to LRU on a fully associative cache, but does not tell us how to think about caches with low associativity, i.e., caches where each page has only 𝑑positions in which it is capable of residing. This means that many modern caches cannot directly apply the result.
<br><br>
It is widely believed that to implement a cache with low associativity, one should still use LRU, but restricted to the 𝑑positions that are eligible for eviction. However, this low-associativity version of LRU has never been analyzed.
<br><br>
We show that low-associativity implementations of LRU are often actually not constant-competitive algorithms. On the other hand, we give randomized eviction algorithms that are constant-competitive, and even a 𝑑-associative algorithm that, using any 𝑑= 𝜔(1), and using 1 + 𝑜(1)resource augmentation, is 1 + 𝑜(1)competitive with the fully-associative LRU algorithm. Combined, our algorithms suggest a new way of thinking about the design of low-associativity caches, in hich one intentionally designs randomized mechanisms that allow parts of the cache which are “overheating” to naturally cool down.
</details>

## The Case for External Graph Sketching
[Download Paper](/assets/papers/2025_external_sketch.pdf)

Michael A. Bender, Martin Farach-Colton, Riko Jacob, Hanna Komlos, David Tench, **Evan T. West**. 2025. The Case for External Graph Sketching. In *Proceedings of the Conference on Applied and Computational Discrete Algorithms (ACDA'25)* (pp. 115-129). Society for Industrial and Applied Mathematics.

<details>
<summary>Abstract</summary>
Algorithms in the data stream model use O(polylog(N)) space to compute some property of an input of size N, and many of these algorithms are implemented and used in practice. However, sketching algorithms in the graph semi-streaming model use O(Vpolylog(V)) space for a V-vertex graph, and the fact that implementations of these algorithms are not used in the academic literature or in industrial applications may be because this space requirement is too large
for RAM on today’s hardware.
<br><br>
In this paper we introduce the external semi-streaming model, which addresses the aspects of the semi-streaming model that limit its practical impact. In this model, the input is in the form of a stream and O(Vpolylog(V)) space is available, but most of that space is accessible only via block I/O operations as in the external memory model. The goal in the external semi-streaming model is to simultaneously achieve small space and low I/O cost.
<br><br>
We present a general transformation from any vertex-based sketch algorithm to one which has a low sketching cost in the new model. We prove that this automatic transformation is tight or nearly (up to a O(log(V)) factor) tight via an I/O lower bound for the task of sketching the input stream.
<br><br>
Using this transformation and other techniques, we present external semi-streaming algorithms for connectivity, bipartiteness testing, (1 + ϵ)-approximating MST weight, testing k-edge connectivity, (1 + ϵ)-approximating the minimum cut of a graph, computing ϵ-cut sparsifiers, and approximating the density of the densest subgraph. These algorithms all use O(Vpoly(log(V),ϵ−1,k) space. For many of these problems, our external semi-streaming algorithms outperform the state of the art algorithms in both the sketching and external-memory models.
</details>

## Exploring the Landscape of Distributed Graph Sketching
[Download Paper](/assets/papers/2025_Landscape.pdf)

David Tench, **Evan T. West**, Kenny Zhang, Michael A. Bender, Daniel DeLayo, Martín Farach-Colton, Gilvir Gill, Tyler Seip, Victor Zhang. 2025. Exploring the Landscape of Distributed Graph Sketching. In *Proceedings of the Symposium on Algorithm Engineering and Experiments (ALENEX'25)*, (pp. 133-146). January 12-13, 2025, New Orleans, LA, USA. SIAM [https://doi.org/10.1137/1.9781611978339.11](https://doi.org/10.1137/1.9781611978339.11)

<details>
<summary>Abstract</summary>
Recent work has initiated the study of dense graph pro- cessing using graph sketching methods, which drastically reduce space costs by lossily compressing information about the input graph. In this paper, we explore the strange and surprising performance landscape of sketching algorithms. We highlight both their surprising advantages for processing dense graphs that were previously prohibitively expensive to study, as well as the current limitations of the technique. Most notably, we show how sketching can avoid bottlenecks that limit conventional graph processing methods.
<br><br>
Single-machine streaming graph processing systems are typically bottlenecked by CPU performance, and distributed graph processing systems are typically bottlenecked by network latency. We present Landscape, a distributed graph-stream processing system that uses linear sketching to distribute the CPU work of computing graph properties to distributed workers with no need for worker-to-worker communication. As a result, it overcomes the CPU and network bottlenecks that limit other systems. In fact, for the connected components problem, Landscape achieves a stream ingestion rate one-fourth that of maximum sustained RAM bandwidth, and is four times faster than random access RAM bandwidth. Additionally, we prove that for any sequence of graph updates and queries Landscape consumes at most a constant factor more network bandwidth than is required to receive the input stream. We show that this system can ingest up to 332 million stream updates per second on a graph with 217 vertices. We show that it scales well with more distributed compute power: given a cluster of 40 distributed worker machines, it can ingest updates 35 times as fast as with 1 distributed worker machine. Graph sketching algorithms tend to incur high computational costs when answering queries; to address this Landscape uses heuristics to reduce its query latency by up to four orders of magnitude over the prior state of the art.
</details>


## Mosaic Pages: Big TLB Reach with Small Pages
[Download Paper](/assets/papers/2024_mosaic_toppicks.pdf)

Krishnan Gosakan, Jaehyun Han, William Kuszmaul, Ibrahim N. Mubarek, Nirjhar Mukherjee, Karthik Sriram, Guido Tagliavini, **Evan West**, Michael A. Bender, Abhishek Bhattacharjee, Alex Conway, Martin Farach-Colton, Jayneel Gandhi, Rob Johnson, Sudarsun Kannan, and Donald E. Porter. Mosaic Pages: Big TLB Reach With Small Pages. *IEEE Micro*. [https://doi.org/10.1137/1.9781611978339.11](https://doi.org/10.1137/1.9781611978339.11)

<details>
<summary>Abstract</summary>
This article introduces mosaic pages, which increase translation lookaside buffer (TLB) reach by compressing multiple, discrete translations into one TLB entry. Mosaic leverages virtual contiguity for locality, but does not use physical contiguity. Mosaic relies on recent advances in hashing theory to constrain memory mappings, in order to realize this physical address compression without reducing memory utilization or increasing swapping. Mosaic reduces TLB misses in several workloads by 6%–81%. Our results show that Mosaic’s constraints on memory mappings do not harm performance, we never see conflicts before memory is 98% full in our experiments—at which point a traditional design would also likely swap. Timing and area analyses on a commercial 28-nm CMOS process indicate that the hashing required on the critical path can run at a maximum frequency of 4 GHz, indicating that a Mosaic TLB is unlikely to affect clock frequency.
</details>


## GraphZeppelin: How to Find Connected Components (Even When Graphs Are Dense, Dynamic, and Massive)
[Download Paper](/assets/papers/2024_GraphZeppelin_TODS.pdf)

David Tench, **Evan West**, Victor Zhang, Michael A. Bender, Abiyaz Chowdhury, Daniel Delayo, J. Ahmed Dellas, Martín Farach-Colton, Tyler Seip, and Kenny Zhang. GraphZeppelin: How to Find Connected Components (Even When Graphs Are Dense, Dynamic, and Massive). In *ACM Transactions on Database Systems* 49, no. 3 (2024): 1-31. [https://doi.org/10.1145/3643846](https://doi.org/10.1145/3643846)

<details>
<summary>Abstract</summary>
Finding the connected components of a graph is a fundamental problem with uses throughout computer science and engineering. The task of computing connected components becomes more difficult when graphs are very large, or when they are dynamic, meaning the edge set changes over time subject to a stream of edge insertions and deletions. A natural approach to computing the connected components problem on a large, dynamic graph stream is to buy enough RAM to store the entire graph. However, the requirement that the graph fit in RAM is an inherent limitation of this approach and is prohibitive for very large graphs. Thus, there is an unmet need for systems that can process dense dynamic graphs, especially when those graphs are larger than available RAM.
<br><br>
We present a new high-performance streaming graph-processing system for computing the connected components of a graph. This system, which we call GraphZeppelin, uses new linear sketching data structures (CubeSketch) to solve the streaming connected components problem and as a result requires space asymptotically smaller than the space required for a lossless representation of the graph. GraphZeppelin is optimized for massive dense graphs: GraphZeppelin can process millions of edge updates (both insertions and deletions) per second, even when the underlying graph is far too large to fit in available RAM. As a result GraphZeppelin vastly increases the scale of graphs that can be processed.
</details>


## Increment-and-Freeze: Every Cache, Everywhere, All of the Time
[Download Paper](/assets/papers/2023_Increment_and_Freeze.pdf)

Michael A. Bender, Daniel DeLayo, Bradley C. Kuszmaul, William Kuszmaul, and **Evan West**. 2023. Increment–and–Freeze: Every Cache, Everywhere, All of the Time. In *Proceedings of the 35th ACM Symposium on Parallelism in Algorithms and Architectures (SPAA ’23)*, June 17–19, 2023, Orlando, FL, USA. ACM, New York, NY, USA, 11 pages. [https://doi.org/10.1145/3558481.3591085](https://doi.org/10.1145/3558481.3591085)

<details>
<summary>Abstract</summary>
One of the most basic algorithmic problems concerning caches is to compute the LRU hit-rate curve on a given trace. Unfortunately, the known algorithms exhibit poor data locality and fail to scale to large caches. It is widely believed that the LRU hit-rate curve cannot be computed efficiently enough to be used in online production settings. This has led to a large literature on heuristics that aim to approximate the curve efficiently.
<br><br>
In this paper, we show that the poor data locality of past algorithms can be avoided. We introduce a new algorithm, called Increment-and-Freeze, for computing exact LRU hit-rate curves. The algorithm achieves RAM-model complexity O(n log n), external-memory complexity O((n/B)log n), and parallelism Θ(log n). We also present two theoretical extensions of Increment-and-Freeze, one that achieves SORT complexity in the external-memory model, and one that achieves a parallel span of 𝑂(log^2 n) which is near linear parallelism, while maintaining work efficiency.
<br><br>
We implement Increment-and-Freeze and obtain a speedup of up to 9x over the classical augmented-tree algorithm on a single processor. On 16 threads, the speedup becomes as large as 60x. In comparison to the previous state-of-the-art parallel algorithm, Increment-and-Freeze achieves a speedup of up to 10x when both algorithms use the same number of threads.
</details>


## Mosaic Pages: Big TLB Reach with Small Pages
[Download Paper](/assets/papers/2023_Mosaic_ASPLOS.pdf)

Krishnan Gosakan, Jaehyun Han, William Kuszmaul, Ibrahim N. Mubarek, Nirjhar Mukherjee, Karthik Sriram, Guido Tagliavini, **Evan West**, Michael A. Bender, Abhishek Bhattacharjee, Alex Conway, Martin Farach-Colton, Jayneel Gandhi, Rob Johnson, Sudarsun Kannan, and Donald E. Porter. 2023. Mosaic Pages: Big TLB Reach with Small Pages. In *Proceedings of the 28th ACM International Conference on Architectural Support for Programming Languages and Operating Systems, Volume 3 (ASPLOS ’23)*, March 25–29, 2023, Vancouver, BC, Canada. ACM, New York, NY, USA, 16 pages. [https://doi.org/10.1145/3582016.3582021](https://doi.org/10.1145/3582016.3582021)

<details>
<summary>Abstract</summary>
The TLB is increasingly a bottleneck for big data applications. In most designs, the number of TLB entries are highly constrained by latency requirements, and growing much more slowly than the working sets of applications. Many solutions to this problem, such as huge pages, perforated pages, or TLB coalescing, rely on physical contiguity for performance gains, yet the cost of defragmenting memory can easily nullify these gains.
<br><br>
This paper introduces mosaic pages, which increase TLB reach by compressing multiple, discrete translations into one TLB entry. Mosaic leverages virtual contiguity for locality, but does not use physical contiguity. Mosaic relies on recent advances in hashing theory to constrain memory mappings, in order to realize this physical address compression without reducing memory utilization or increasing swapping.
<br><br>
This paper presents a full-system prototype of Mosaic, in gem5 and modified Linux. In simulation and with comparable hardware to a traditional design, mosaic reduces TLB misses in several workloads by 6–81%. Our results show that Mosaic’s constraints on memory mappings do not harm performance, we never see conflicts before memory is 98% full in our experiments — at which point, a traditional design would also likely swap. Once memory is over-committed, Mosaic swaps fewer pages than Linux in most cases. Finally, we present timing and area analysis for a verilog implementation of the hashing function required on the critical path for the TLB, and show that on a commercial 28nm CMOS process; the circuit runs at a maximum frequency of 4 GHz, indicating that a mosaic TLB is unlikely to affect clock frequency.
</details>


## GraphZeppelin: Storage Friendly Sketching for Connected Components on Dynamic Graph Streams
[Download Paper](/assets/papers/2022_GraphZeppelin_SIGMOD.pdf)

David Tench, **Evan West**, Victor Zhang, Michael A. Bender, Abiyaz Chowdhury, J. Ahmed Dellas, Martín Farach-Colton, Tyler Seip, and Kenny Zhang. 2022. GraphZeppelin: Storage-Friendly Sketching for Connected Components on Dynamic Graph Streams. In *SIGMOD ’22: ACM Special Interest Group on Management of Data*, June 12–17, 2022, Philadelphia, PA. ACM, New York, NY, USA, 15 pages. [https://doi.org/10.1145/3514221.3526146](https://doi.org/10.1145/3514221.3526146)

<details>
<summary>Abstract</summary>
Finding the connected components of a graph is a fundamental prob- lem with uses throughout computer science and engineering. The task of computing connected components becomes more difficult when graphs are very large, or when they are dynamic, meaning the edge set changes over time subject to a stream of edge inser- tions and deletions. A natural approach to computing the connected components on a large, dynamic graph stream is to buy enough RAM to store the entire graph. However, the requirement that the graph fit in RAM is prohibitive for very large graphs. Thus, there is an unmet need for systems that can process dense dynamic graphs, especially when those graphs are larger than available RAM.
<br><br>
We present a new high-performance streaming graph-processing system for computing the connected components of a graph. This system, which we call GraphZeppelin, uses new linear sketching data structures (CubeSketch) to solve the streaming connected components problem and as a result requires space asymptotically smaller than the space required for a lossless representation of the graph. GraphZeppelin is optimized for massive dense graphs: GraphZeppelin can process millions of edge updates (both insertions and deletions) per second, even when the underlying graph is far too large to fit in available RAM. As a result GraphZeppelin vastly increases the scale of graphs that can be processed.
</details>


## Paging and the Address-Translation Problem
[Download Paper](/assets/papers/2021_AddressTranslation.pdf)

Michael A. Bender, Abhishek Bhattacharjee, Alex Conway, Martín Farach-Colton, Rob Johnson, Sudarsun Kannan, William Kuszmaul, Nirjhar Mukherjee, Don Porter, Guido Tagliavini, Janet Vorobyeva, and **Evan West**. 2021. Paging and the Address-Translation Problem. In *Proceedings of the 33rd ACM Symposium on Parallelism in Algorithms and Architectures (SPAA ’21)*, July 6–8, 2021, Virtual Event, USA. ACM, New York, NY, USA, 13 pages. [https://doi.org/10.1145/3409964.3461814](https://doi.org/10.1145/3409964.3461814)

<details>
<summary>Abstract</summary>
The classical paging problem, introduced by Sleator and Tarjan in 1985, formalizes the problem of caching pages in RAM in order to minimize IOs. Their online formulation ignores the cost of address translation: programs refer to data via virtual addresses, and these must be translated into physical locations in RAM. Although the cost of an individual address translation is much smaller than that of an IO, every memory access involves an address translation, whereas IOs can be infrequent. In practice, one can spend money to avoid paging by over-provisioning RAM; in contrast, address translation is effectively unavoidable. Thus address-translation costs can sometimes dominate paging costs, and systems must simultaneously optimize both.
<br><br>
To mitigate the cost of address translation, all modern CPUs have translation lookaside buffers (TLBs), which are hardware caches of common address translations. What makes TLBs interesting is that a single TLB entry can potentially encode the address translation for many addresses. This is typically achieved via the use of huge pages, which translate runs of contiguous virtual addresses to runs of contiguous physical addresses. Huge pages reduce TLB misses at the cost of increasing the IOs needed to maintain contiguity in RAM. This tradeoff between TLB misses and IOs suggests that the classical paging problem does not tell the full story.
<br><br>
This paper introduces the Address-Translation Problem, which formalizes the problem of maintaining a TLB, a page table, and RAM in order to minimize the total cost of both TLB misses and IOs. We present an algorithm that achieves the benefits of huge pages for TLB misses without the downsides of huge pages for IOs.
</details>
