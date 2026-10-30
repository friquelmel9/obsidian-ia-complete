---
tags:
  - cs/optimization
aliases:
---
# $K$-Graph-Coloring Problem

The $K$-[[Graph]]-Coloring Problem is a generalization of the $3$-Graph-Coloring Problem

In a Graph, assign a color to each node where each connected node doesn't share colors

![[K-Color.png]]
## CSP/CSOP Problem

This problem can be defined as a [[Constraint Satisfaction Problem|CSP/CSOP]]

- **Variables**: 
	- $x_i$ the color of the $i$ node
- **Domain:**
	- The $k$ colors. $D_{x_i} = \{1,2,\dots,k\}$
- **Constraints:
	- Edges: Each edge restriction must check that the colors are different. That means $x_i  \neq x_j$

