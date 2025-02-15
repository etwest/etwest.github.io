---
layout: post
title: Presentation of GraphZeppelin at Graduate Research Day
lead: Presented my paper on computing the connected components of a dynamic graph stream at Stony Brook University's computer science graduate research day.
---

[![](/assets/files/GraphZeppelin-GRD'22.pdf)](/assets/files/GraphZeppelin-GRD'22.pdf)

## Graduate Research Day
Graduate Research Day is an event put on by the Stony Brook Computer Science Department in which graduate students (primarily Ph.D. students) present their research to peers and a panel of judges. Students submit posters to present and some are selected to give talks. The day is divided into talk sessions, the poster presentation, and an awards ceremony. Awards are given to the best overall talk and poster, and to the best posters and talks within subject areas (Systems, ML, or Theory).

I was selected to give a talk, and my talk was selected as the best theory presentation.

## Topic of Talk
Computing properties of graphs becomes very difficult when the graph is large and dense. That is, when storing the graph losslessly exceeds the resources of the machine (RAM or Disk). This problem becomes even more challenging when the graph is constructed by a dynamic stream. Dynamic graph streams iteratively insert or delete edges and the property must be computed after the stream concludes.

We present a new high-performance streaming graph-processing system for computing the connected components of a graph. This system, which we call *GraphZeppelin*, uses new linear sketching data structures (CubeSketch) to solve the streaming connected components problem and as a result requires space asymptotically smaller than the space required for a lossless representation of the graph. GraphZeppelin is optimized for massive dense graphs: GraphZeppelin can process millions of edge updates (both insertions and deletions) per second, even when the underlying graph is far too large to fit in available RAM. As a result GraphZeppelin vastly increases the scale of graphs that can be processed.

See [the paper](/assets/papers/2024_GraphZeppelin_TODS.pdf) for more information.
