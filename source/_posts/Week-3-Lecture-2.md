---
title: Week 3 Lecture 2
date: 2019-03-15 11:04:03
tags:
---

## Matrices

### Matrices to the rescue

Matrices allow us to easil manage transformations. Different transformations are the same size (think of them as shipping containers). Matrices can be combined.

### Matrices in WebGL

THANKS. I hate it.

WebGL allow us to easily talka bout matrices. However, one major differences is that WebGL matrices are ***transposed*** from how we normally deal with them. Tou will need to take this into account when writing matrix code.

```Javascript
/*

OG Matrix:

ix, jx, Tx
iy, jy, Ty,
 0,  0,  1

*/

// Trnasposed WebGL Matrix
const matrix = [
    ix, iy, 0,
    jx, jy, 0,
    Tx, Ty, 1
];
```
