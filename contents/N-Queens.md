---
tags:
  - cs/optimization
aliases:
---
# N-Queens

The N-Queen Problem is a generalization of the 8-Queen Puzzle. 

Place $N$ queens on an $N\times N$ board so that no two queens can attack each other. 

## CSP Model

The model can be define as an [[Constraint Satisfaction Problem|CSP]].

- **Variables**:
	- $x_i$: The $N$ queens ($x_1,x_2,\cdots,x_n$), which each queen index representing their row
- **Domain:** 
	- $D_{x_i}$: The position of the column where the queen is placed
- **Constraints:** 
	- No same column: $x_i \neq x_j$
	- No same diagonal: $|Q_i - Q_j| \neq |i-j|$

> [!note] 
> We use the queens to represent the row to have a smaller search space.
> If we use the variable $x_i$ as "The $i$ queen" with domain $D_{x_i} = \{1,2,3,\dots,n\times n\}$, then the search space will be $(n^{n\times n})$