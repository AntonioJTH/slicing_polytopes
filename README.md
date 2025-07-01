# Hypercube Slice Analysis

This repository contains a Python implementation to compute all slices of a hypercube in specified directions (Directions for the Slices Q_6 and Q_7.ipynb). The vertices of the hypercube are restricted to have entries in {-1, 1}, representing a `d`-dimensional binary cube.

## Overview

The program takes a set of directions (vectors) as input and computes the slices of the hypercube in those directions. For each direction, it:
1. Orders the vertices of the hypercube based on their dot product with the direction vector.
2. Computes the number of "cuts" (intersections) for both vertices and edges when slicing the hypercube along planes orthogonal to the given direction.

## Features

- Handles hypercubes of arbitrary dimensions (`d`).
- Supports precision-based calculations using fractions.
- Computes slices for a user-defined set of direction vectors.
- Outputs all unique slices for the given directions.

## Input

The program expects a list of directions, where each direction is represented as a list of floats or fractions. For example:

```python
directions = [
    [1.0, 1.0, -0.9, -0.9, -0.5, -0.5],
    [1.0, 1.0, -0.9, -0.9, -0.5, 0.0],
    [Fraction(3, 500), Fraction(3, 1000), Fraction(7, 1000), Fraction(3, 500)]
]
