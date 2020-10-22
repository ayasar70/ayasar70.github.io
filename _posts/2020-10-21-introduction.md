---
title: Partitioning
date: 2020-10-21
categories: text
---


![GitHub Logo](/assets/images/ay.png)<br />

Given two graphs, graph merging problem involves identifying each vertex in a graph with a corresponding vertex (i.e., representing the same entity) in the other graph, whenever such corresponding vertices exist. This problem is known to be NP-complete [72]. Most of the state-of-the-art solutions have high computation complexity and rely on a similar- ity matrix [7, 72, 149, 74] whose computation requires quadratic (in terms of the number of vertices) run time. We propose a novel, fast graph merging algorithm, GSANA [143]. GSANA partitions the “computation space” to reduce the computational complexity of the problem. GSANA takes a divide-and-conquer approach and partitions the vertices into buckets. GSANA then compares the vertices of the first graph in a bucket with the vertices of the second graph that are in the same bucket. The novelty of the proposed approach is to use the global structure of the graph to partition the vertices into buckets (blocks). Such computation partitioning is very useful to solve hard graph problems that require quadratic all pair comparisons. We also propose a parallel network aligner called SINA, in which we parallelize all costly components of GSANA. In SINA [145], we investigate an efficient and scalable parallelization of GSANA without sacrificing its recall. We implement the find- ings in a data-parallel, architecture (resource)-aware scalable graph alignment framework. We also investigate two parallelization strategies for similarity computations and also two graph layout strategies for an emerging architecture, Emu Chick [51].