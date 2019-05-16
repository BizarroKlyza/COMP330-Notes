---
title: Week 9 Lecture 1
date: 2019-05-09 10:59:39
tags:
---

# Lighting

Lights are one of the major cues for adding depth to a 3D scene.

Lighting is affected by:
* Source position, direction, brightness, colour, size, polarisation
* Surface position, orientation, material, colour
* Camera position
* Possible pathways for light to travel
* Medium (air, water, smoke), wave properties, etc

## Direct Lighting

## Indirect Lighting

Indirect lighting considers light htat travels longer paths

## Physics

We use heavily simplified model of the physics of light:
* Consider an **incident ray** coming from a source hitting a surface
* Calculate the intensity of the **reflected ray** in the direction of the camera

## Materials

Different surface materials refelct light in different ways:
* Matte surfaces (e.g., paper) exhibit **diffuse** reflection. Incoming light is reflected equally in all directions.
* Polished surfaces (e.g., plastic) exhibits **specular** relfection. Incoming light is mostly reflected in a particular direction
* Other materials (e.g., skin, metal, water) have more complex properties

## Diffuse reflection

The amount of reflected light is inversely proportional to the area of the face subtended by the source. I.e., intensity of reflection is lower at oblique angles

## Lambert's Law

Angle between two vectors is dot product of two normalised vectors

## Diffuse reflection coefficient

The coefficient `pd` is a property of the surface.
* Light surfaces have values close to 1
* Dark surfaces have values close to 0

## Specular reflection

Only mirrors exhibit perfect specular reflection. On other surfaces there is still some scattering.

Intensity falls off based on the angle between the reflected vector `r` and the view direction `v` (i.e., vector toward the camera)

## Phong model

The **Phong reflection model** is an approximate model of specular reflection. It allows us to add highlights to shiny surfaces. It looks good for plastic and glass but not good for polished metal (in which real reflections are more visible).

### Phong exponent

Larger values of the Phong exponent `f` produce less scattering, creating more mirror-like surfaces.

## Reflection

Note that the Phong model only reflects **light sources**, not the environment. It is good for adding bright highlights but cannot create a true mirror. Proper reflections are more complex to compute.

## Ambient light

Lighting with just diffuse and specular lights gives very stark...

## Colour

We implement colour by having separate red, green, and blue components for:
* Light intensities
* Reflection coefficients

The lighting equation is applied three times, once for each colour.
