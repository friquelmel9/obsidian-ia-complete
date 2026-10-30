---
tags:
  - cs/optimization
aliases:
  - Arc-Consistent
---
# Arc Consistency

A variable in a [[Constraint Satisfaction Problem|CSP/CSOP]] is **arc-consistent** if every value in its domain saitsfies the variable's binary constraints. 

Formally speaking, $x_i$ is arc consistent with respect to another variable $x_j$ if for every value in the current domain $D_{x_i}$ there is a value in $D_{x_j}$ that satisfies the binary constraint on the arc $(x_i,x_j)$. [^2]

> [!important] 
> If an [[Constraint Satisfaction Problem|CSP/CSOP]] has a solution, the solution must be arc-consistent. However, being arc-consistent doesn't mean that the problem has a solution.
> ![[Arc Consistent without Solution.png]]

## Process

This example is for two variables with the binary constraint $x_1 > x_2$.

![[Arc Consistency.png]]

[^1]

[^1]: Obtenido de la Ayudantia 2 de 2026-2

[^2]: Obtained from [[Artificial Intelligence - A modern Approach]], page 170
