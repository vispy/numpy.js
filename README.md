numpy.js
========

This is a *very basic* NumPy-like JavaScript library. It is required by our Python->JavaScript translator. Written in vanilla JavaScript, it aims at supporting a minimal set of routines for the most common use-cases in numerical computing. Eventually, the goal is to have a translator that takes relatively simple Python/NumPy functions and translates them to JavaScript. Typically, these functions will be interactivity functions (like callback functions reacting to mouse movements, key strokes...) and emitting GLIR (OpenGL) commands to update the visualization.

The first step here is to look at @mikolalysenko's [ndarray](https://github.com/mikolalysenko/ndarray) library (MIT license) and see if we can reuse some of the code. Otherwise, we can as well start from scratch.


## Features

* `ndarray` structure (dtype, shape, strides, C-order/FORTRAN-order)
* `zeros`, `ones`, `eye`, `array`, `linspace`, `diagonal`
* views (without underlying copies)
* data types to support: `float32`, `float64`, `(u)int8|16|32`
* indexing with `get(i, j, ...)` and `set(i, j, ..., v)`
* `slice(start, stop, step)` object, understood by indexing operators
* `transpose`, `reshape`, `repeat`, `flatten`
* `copy`
* element-wise operations (`+, -, *, /, %`)
* element-wise mathematical functions (`cos`, `exp`, `log`, etc.)


## Optional features

From this minimal set of core features, additional features can be implemented later as needed.

* `min`, `argmin`, `mean`, `std`, etc.
* `clip`, `cumsum`, `sum`, etc.
* `dot`

