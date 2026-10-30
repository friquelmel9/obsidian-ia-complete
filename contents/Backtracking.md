---
tags:
  - cs/algorithm
  - cs/optimization
aliases:
---
# Backtracking

Backtracking algorithms are problem-solving [[Algorithm]] that help explore different options to find the solution. Work by trying out different paths and if one doesn't work, then backtrack and try another until he right one is found. [^1]

## CSP

When solving an [[Constraint Satisfaction Problem|CSP/CSOP]], there's an ordering of variables and domains. The most common one is to go from left to right (numerical order, such as $x_1, x_2$, and so on) or use [[Heuristic Techniques]] such as [[Minimum Remaining Value Heuristic|MRV]] techniques.

### Example

In the next image, backtracking goes to the node previous instanced variable, being $D$ (purple link)

![[Backtracking vs GBJ vs CBJ.png]]

[^1]: Obtained from https://www.geeksforgeeks.org/dsa/backtracking-algorithms/
