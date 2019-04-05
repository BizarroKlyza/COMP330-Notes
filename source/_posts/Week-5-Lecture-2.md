---
title: Week 5 Lecture 2
date: 2019-03-29 10:40:01
tags:
---

## Fragment Shaders

We're almost done with vertex shaders. (How?) We know pretty much everything there is to know about vertex shaders at this point. (Again, HOW?) We've just started in 3d, buut there isn't any new concepts for vertex shaders. There is one last part, projection, that will be covered next week. (maybe) We want to know about projection.

Fragment shaders determine the final pixel color. The run for **every** fragment (pixel) that a shape will cover. Written in GLSL like vertex shaders.

### Varyings

Varyings are how you pass information from the vertex shader to the fragment shader (that isn't global, that's what uniforms are for). They match by name, all you need to do is have a matchig variable in your vertex shader and fragment shader and webgl will link them.

WebGL interpolate values for color.
