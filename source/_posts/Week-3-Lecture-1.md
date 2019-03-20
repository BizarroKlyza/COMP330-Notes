---
title: Week 3 Lecture 1
date: 2019-03-14 11:08:16
tags:
---

## 2D Transformations

### Translation

```Javascript
Xw = Xm + Tx
Yw = Ym + Ty
```
```Javascript
translate(Tx, Ty)
T(Tx, Ty) # means translation
T(1, 0) # translate X by 1 unit
```

### Rotation

```Javascript
rotate(toRadian(A))
```

### Scale

```Javascript
Xw = Xm.Sx
Yw = Ym.Sy
Scale(Sx, Sy)
S(Sx,Sy)
```

### Shear

```Javascript
Xw = Xm + bxYm
Yw = Ym + bxXm
```

### Combining Transformations

**TRaSHEes**

```Javascript
T( )
R( )
SH( )
S( )
```

Put them in the correct order so you don't *trash* your code.

## Let's get into some MATH

### Scale

```Javascript
Xw = Xm.Sx
Yw = Ym.Sy
```
`jamie will add in the drawing of the matrices`
```Javascript
Xw = SxXm + 0Ym
Yw = SyYm + 0Xm
```
`jamie will add in the drawing of the matrices`

### Shear

`jamie will add in the drawing of the matrices`

### Rotate
```Javascript
Xw = cos(theta).Xm - sin(theta).Ym
Yw = sin(theta).Xm + cos(theta).Ym
```

`jamie will add in the drawing of the matrices`

## Homogenous Coordinates

`images to be added maybe by ya boi`
