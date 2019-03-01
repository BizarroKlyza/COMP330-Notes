---
title: Week 1 Lecture 2
date: 2019-03-01 11:09:27
tags:
---

## Why JavaScript?!

WebGL is really good for beginners. Modern and up to date (but not bleeding edge). It's very portable (runs in browser). Javascript is *relatively* easy to learn.

## Use a sane browser

Use Firefox Developer Edition. It allows things like like shader code editing which will be useful. Chrome is good too as its error messages are sometimes better than Firefox. Edge is decent. Safari is trash. IE is complete garbage.

## Boilerplate HTML file

```html
<!DOCTYPE html>
<html>

<head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Week 1</title>
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
        start();
    </script>
</body>

</html>
```
