---
title: Week 1 Lecture 1
date: 2019-02-28 17:50:37
tags:
---

*Contributors: Anthony Klyza, Elise McCabe, Jamie Simpson*

## What is computer graphics
Computer graphics is about producing images or animations.
A model is the data it takes to describe a scene, which is then run through multiple processing steps to generate an image.
OpenGL is a library that does the graphics work for you. It is almost a language.
It is similar to an API, which we can call using Javascript.
### Raster Graphics
Here we have pixels, each pixel contains a colour, most will have 8 bits per pixel, which contains values `0-255`. These values are repeated 3 times for Red, Green
and Blue.
Now that we have this raster we need a way to refer to it. We use a coordinate
format for this.

## The CPU
The cpu can communicate with the graphics processor over the system bus which
generates data and stores it in the Frame buffer.

This is memory that corresponds
to the pixels on the screen. The frame buffer is on the graphics card. What we want
to do is generate an image on the screen so we need to take the colour values out
of here and send them as pixels to the display controller.

What this does is reads
out the rgb values for each pixel and sends it to the display as a voltage value. How
fast it does this is the FPS of the display. I.E., a 60Hz display will read out of the frame
buffer 60 times per second. The graphics processor writes data into the frame buffer and the display controller will read out of it.

## Computer Graphics Pipeline

Computer graphics starts with a model that defines a load of points in 3d
space.
We connect these together with 2d shapes such as triangles.

### Handout 1.1

* Pipeline

    Sequence of steps we go through to process data and produce an end result.

* (Geometric) Transform

    Takes points in one coordinate system and applys in another coordinate system. Applies matrices to coordiantes.

* Viewport

    Portion of screen that displays rendered image.

* Clipping

    ...

* Rasterisation

    ...

* Texture mapping

    Wraps a texture aimage around an object.

* Blending

    ...

* Depth buffering

    ...

* Alpha value

    Transparency value.

* Shader program

    ...

* Color quantisation

    Mapping one color range to another.
