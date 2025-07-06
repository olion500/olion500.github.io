---
layout: post
title: "LCA (Lowest Common Ancestor)
date: 2022-07-26 21:24:33
categories: algorithm
---

# LCA 
The Lowest Common Ancestor(LCA) of two nodes a, b in a tree or directed acyclic graph (DAG) T is the lowest node that has both a and b as descendants, where we define each node to be descendant of itself (so if a has a direct connection from b, b is the lowest common ancestor).

LCA can be reduced into RMQ first, then divided the sequence of numbers into intervals and apply two different techniques to handle range minimum query across different intervals, and handle range minimum query iwthin an interval.

## Reduction from LCA to RMQ
Reduction of LCA into RMQ started by walking the tree. When walking the tree, the order of the label and ethe depth of the node visited is recorded. Then a LCA question can be answered by answering a RMQ question which the input of a RMQ problem is the indices of two child nodes in the list of visited nodes.

![LMC_to_RMQ](https://user-images.githubusercontent.com/13013735/181005644-4d2f413b-164f-4d50-95db-21fefe7bcf74.png)

Therefore, LCA can be solved by solving RMQ.
