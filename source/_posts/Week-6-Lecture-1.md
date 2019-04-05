---
title: Week 6 Lecture 1
date: 2019-04-04 10:55:21
tags:
---

## Projections

### Orthographic

If you move the camera closer or further to an object, they stay the same size.

#### Simple Orthograpic Projection

Compute x,y,z in camera <br>
Set `z = 0 or -1` (fixed value)

#### Define equation for x'

Convert range (l,r) to (-1,1) <br>

`x(2/(r-l) - ((r+l)/(r-l))`

### Perspective

Objects closer to the focal point appear larger and objects further appear smaller. Like eyes.

#### Simple Perspective Projection

Divide the vector XYZ by -Z
