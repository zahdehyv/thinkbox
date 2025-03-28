---
type: wiki
subType: ""
title: Wavelet Tree
englishTitle: Wavelet Tree
year: ""
dataSource: Wikipedia API
url: https://en.wikipedia.org/wiki/Wavelet_Tree
id: 36038546
wikiUrl: https://en.wikipedia.org/wiki/Wavelet_Tree
lastUpdated: 2025/February/25
length: 5236
tags: mediaDB/wiki
---
 The **Wavelet Tree** is a succinct data structure to store strings in compressed space. It generalizes the ${\displaystyle \mathbf {rank} _{q}}$ and ${\displaystyle \mathbf {select} _{q}}$ operations defined on bitvectors to arbitrary alphabets.

 Originally introduced to represent compressed suffix arrays, it has found application in several contexts. The tree is defined by recursively partitioning the alphabet into pairs of subsets; the leaves correspond to individual symbols of the alphabet, and at each node a bitvector stores whether a symbol of the string belongs to one subset or the other.

The name derives from an analogy with the [[Wavelet transform|wavelet transform]] for signals, which recursively decomposes a signal into low-frequency and high-frequency components.