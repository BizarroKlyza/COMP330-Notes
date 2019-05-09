---
title: Week 8 Lecture 1
date: 2019-05-02 11:07:38
tags:
---

# Depth and Transparency

*It's a per sample operation*

Take fragments from rasterization and determine which to put on screen.

## Painter's algorithm

The naive approach to hidden surface removal.
* Sort polygons by depth
* Draw in order from back to front

Sorting triangles, bad. Sorting pixels, good.

## Z-buffering

For each pixel, keep a **z-buffer** (or **Depth-buffer**):

```
depth[x,y] = current depth of fragment at (x,y)
```

## Depth

In reality depth values are floating point values between -1 (near plane) and 1 (far plane).

## Z-Fighting

Rounding errors in perspective calculates can create artefacts when triangles shapes closely overlap.

Solution:
* Adjust the near and far planes to give more precision
* Move the objects so there is always a slight gap between them

## Occlusion Culling

In a complex world with many overlapping objects, we may still be writing to the depth and color buffers many times.

Ideally, we would like to not even generate fragments that are not going ot be displayed on screen.

**Occlusion culling** is the name for a variaty of techniques that aim to cull geometry that  is occluded (i.e., hidden behind something else).

Algorithms for occlusion culling are complex and beyong the scope of this course.

## Transparency

A transparent (or translucent) object lets some of the light through from the object behind it.

### The alpha channel

When we specify colors we have used for components:
* red/green/blue
* alpha - the **opacity** of the color

alpha = 1 means the object is opaque

alpha = 0 means the object is completely transparent (invisible)

`c = (r,g,b,a)`

### Alpha blending

When we draw one object over another, we can blend their colors according to the alpha value.

There are many blending equations, but the usual one is ***LERPing***.

### Problem

Alpha blending depends on the order that pixels are drawn.

You need to draw transparent polygons after the polygons behind them.

If you are using the depth buffer and you try to draw the transparent polygon before the objects behind it, the later objects will not be drawn.

### Solution

To solve this we need to sort all fragments in terms of depth and draw them from back to front.

In practice this is considered too expensive.

### Soultions (sort of)

Instead:
* Draw all opaque objects first, then the transparent objects
* Completely transparent fragments (alpha = 0) can be ignored
* Sort all the transparent trianbles based on z distance and draw in order from back to from (Painter's algorithm)

This still encounters the ordering problem we discussed earlier.
