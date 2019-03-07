---
title: Week 1 Lecture 2
date: 2019-03-01 11:09:27
tags:
---

*Contributors: Anthony Klyza, Jamie Simpson*

***Dont use var in Javascript***

## Why JavaScript?!

WebGL is really good for beginners. Modern and up to date (but not bleeding edge). It's very portable (runs in browser). Javascript is *relatively* easy to learn.

## Use a sane browser

Use [Firefox Developer Edition](https://www.mozilla.org/en-US/firefox/developer/). It allows things like like shader code editing which will be useful. Chrome is good too as its error messages are sometimes better than Firefox. Edge is decent. Safari is trash. IE is complete garbage.

## Variables

```Javascript
var c = 10;
const x = 20;
let y = 3;
```

There are 3 ways of defining variables in js, `const` will not let it be changed, if we
are initialising a variable use `const` and if we get yelled at use `let`.

**Use [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript) as a reference for documentation explaining pieces of code in
the unit.**

`==` refers to equality of value not equality of type, because fuck logic, this
means if we run
```Javascript
0 == "0"
-> true
```
`===` refers to complete equality which means if we run
```Javascript
0 === "0"
-> false
```

Javascript and shaders compile at runtime causing any compilation errors to appear at runtime rather than precompiled due to the wide range of systems and
graphics cards they’re being run on.
Putting `use strict` on a program will make the browser check types

## Boilerplate HTML file

```html
<!DOCTYPE html>
<html>

<head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Yeet</title>
    <script src="main.js"></script>
    <style>
        html,
        body {
            margin: 0;
            padding: 0;
        }

        canvas {
            display: block;
        }
    </style>
</head>

<body>
    <script type="text/javascript">

    </script>
</body>

</html>
```

## What did we learn today?

**NOTHING**

*Thanks Peter*
