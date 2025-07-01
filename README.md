# Hypercube Slice Analysis

This repository contains a Python implementation to compute all slices of a hypercube in specified directions (Directions for the Slices Q_6 and Q_7.ipynb). The vertices of the hypercube are restricted to have entries in {-1, 1}, representing a `d`-dimensional binary cube.

## Overview

The program takes a set of directions (vectors) as input and computes the number of verties on the slices of the hypercube in those directions. For each direction, it:
1. Orders the vertices of the hypercube based on their dot product with the direction vector.
2. Uses the sequence of vertices and edges induced by the direction to compute the number of vertices that appear in the slices defined by hyperplanes orthogonal to that direction.


## Input

The program expects a list of number of vertices obtenidos por todos los cortes posibles en las direcciones dadas, where each direction is represented as a list of floats or fractions. For example:

```python
directions = [
    [1.0, 1.0, -0.9, -0.9, -0.5, -0.5],
    [1.0, 1.0, -0.9, -0.9, -0.5, 0.0],
    [Fraction(3, 500), Fraction(3, 1000), Fraction(7, 1000), Fraction(3, 500)]
]
```

## Output

For each direction, the program returns a list of values (the number of vertices) corresponding to slices defined by hyperplanes orthogonal to that direction. It also accumulates all values found across all directions. For example:

```python
Accumulated slices: {7, 12, 16, 17, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50, 51, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 64, 65, 66, 67, 68, 69, 70, 71, 72, 73, 74, 75, 76, 77, 78, 79, 80, 81, 82, 83, 84, 85, 86, 87, 88, 89, 90, 91, 92, 93, 94, 95, 96, 97, 98, 99, 100, 101, 102, 103, 104, 105, 106, 107, 108, 109, 110, 111, 112, 113, 114, 115, 116, 117, 118, 119, 120, 121, 122, 123, 124, 125, 126, 127, 128, 129, 130, 131, 132, 133, 134, 135, 136, 137, 138, 139, 140}
```
