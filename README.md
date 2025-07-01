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


## Output

For each direction, the program returns a list of values of $\nu$ (the number of vertices) corresponding to slices defined by hyperplanes orthogonal to that direction. It also accumulates all values found across all directions.
