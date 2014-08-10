---
title       : Small World Network
subtitle    : A brief note after studying "Is Boston Subway a Small World Network?"
author      : Yusan Lin
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : prettify  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : mathjax            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Notations

$N$: number of nodes

$K$: number of edges

$\{ a_{ij} \}$: adjacency matrix

$\{ l_{ij} \}$: spatial distance between nodes

$d_{ij}$: the shortest path between $i$ and $j$

$L = \frac{1}{N(N-1)} \sum_{i \neq j} d_{ij}$: average distance

$c_i = \frac{\text{number of edges}}{k_i(k_i - 1)/2}$: clustering coefficient

$C = \frac{1}{N} \sum_{i} c_i$: average clustering coefficient

--- .class #id 

## Extension from original Small World Network model

### Notation

Instead of just considering the $L$ and $C$, this approach also considers the *efficiency*:

$\epsilon_{ij} = \frac{1}{d_{ij}} \forall i,j$: efficiency between $i, j$

$E = \frac{1}{N(N-1)} \sum_{i \neq j} \epsilon_{ij} = \frac{1}{N(N-1)} \sum_{i \neq j} \frac{1}{d_{ij}}$: average efficiency over the whole network

### Test

$E_{\text{glob}}$: efficiency of whole network

$E_{\text{loc}}$: average efficiency of the subgraph of the neighbors

For small network, it has both high $E_{\text{glob}}$ and high $E_{\text{loc}}$.

--- .class #id

## Cost

This work also considers the **cost** of the network:

$\text{Cost} = \frac{\sum_{i \neq j} a_{ij} l_{ij}}{\sum_{i \neq j}l_{ij}}$
