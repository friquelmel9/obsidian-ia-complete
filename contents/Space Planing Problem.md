---
tags:
  - cs/optimization
aliases:
---
# Space Planning Problem

The space planning problem states that given an area and a set of figures, the figures must be put inside the bigger area.

![[Space Planning.png]]

> [!seealso] 
> The space planning problem assumes discrete and orthogonal positions, that means, the edges are all paralel from each other like a grid, 
> Removing the orthogonality leads to a [[Nesting Problem]]

## Model

The Space Planning problem can be modeled as an [[Constraint Satisfaction Problem|CSP/CSOP]]

- **Variables**: With $i \in  \{1,\cdots, F\}$
	- $x_i$: The horizontal position for piece $i$.
	- $y_i$: The vertical position for piece $i$
	- $r_i$: If piece $i$ is rotated $90$ degrees
- **Domain**:
	- $D_{x_{i}} \in \{0,\cdots,L\}$
	- $D_{y_{i}} \in \{0,\cdots,H\}$
	- $D_{r_i} \in \{0,1\}$. Binary decision if the figure is rotated.
- **Parameters**:
	- $F$: The number of figures available
	- $l_{i}, h_{i}$: The horizontal and vertical length of the figure $i$
	- $L,H$: The horizontal lenght $L$ and the vertical height $H$ of the area.
	- $f_{l_i} = l_i(1-r_i) + h_i(r_i)$: Function that returns the true horizontal length if rotated
	- $f_{h_i} = h_i(1-r_i) + l_i(r_i)$: Function that returns the true vertical length if rotated
- **Constraints**: with $i,j \in \{1,\cdots,F\}$
	- The figures must be inside the area. $$\begin{aligned} x_{i} + f_{l_i} \leq L ~ ~ \forall i \\ y_i + f_{h_i} \leq H ~ ~ \forall i\end{aligned}$$
	- No figures must overlap. $$\begin{aligned} x_i +f_{l_i} \leq x_j ~ ~ \forall ~ i \neq j\\ y_i + f_{h_i}\leq y_j ~ ~ \forall ~ i \neq j\end{aligned}$$

Depending on the problem, an objective function can be used to convert the problem into an [[Constraint Satisfaction Problem|CSOP]].
- Minimizing the height $$\min f = \max{(y_i + f_{h_i})}$$