---
tags:
  - cs/optimization
aliases:
---
# Constraint Graph

An Constraint [[Graph]] is a graph that indicates the restrictions for a [[Constraint Satisfaction Problem|CSP/COP]] problem.

- Each node is a variable
- Each edge indicates there's **one or more** restrictions for the pair of variables

A constraint graph can only be made from Binary Constraints [^1], If there are more constraints then is a multi-dimensional Constraint Graph [^2]

## Example

Consider the restrictions on the left, with variables $x_1$ to $x_5$.
![[Constrained Graph.png]]

[^1]: See [[Constraints in CSP#Variable Types]]

[^2]: Realmente no se como se llama. Tiene un nombre especifico, pero la idea se mantiene. Es un grafo de mayor dimensión
