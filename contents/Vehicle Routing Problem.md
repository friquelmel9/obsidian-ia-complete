---
tags:
  - cs/optimization
aliases:
  - VRP
---
# Vehicle Routing Problem

In a vehicle Routing Problem, we are given n nodes that we have to visit from a starting point (generally considered a depot).

We have multiple routes to take, and all the vehicles start from depot, visit $k$ nodes, and then they must go back into the starting point.

![[VRP.png]]
## Model

Vehicle Routing Problem can be modeles as an [[Constraint Satisfaction Problem|CSOP]]

> [!note] Notación
> Usar la variable $V^k$ indica que para cada elemento de $k$ tendre una variable nueva. Es decir, si $k \in \{1,2,3\}$, entonces existiran las variables $V1_{ij}$, $V2_{ij}$ y $V3_{ij}$

- **Variables**:
	- $V^k_{ij}$: Vehicle $k$ goes from node $i$ to node $j$
- **Domains**
	- $D_{V^k_{ij}}$: Binary decision $\{0,1\}$
	- $i \in I$, $j \in I$ and $j \in K$, where each set has the enumerated values 
		- e.g : $I = \{1,2,... \}$
- **Parameters**:
	- $c_{ij}$: Cost of traveling from node $i$ to node $j$
	- $w_i$: Weight for the node $i$, generally meaning how much product does need
	- $M_k$: Max weight for the vehicle $k$
- **Restriction**
	- All nodes must be visisted once $$\sum_{k\in K}\sum_{i \in I}V^k_{ij} = 1 ~ ~ \forall j \tag{i}$$
	- If it goes to one node, it must then go from it $$$$

> [!danger] Sobre usar la expresión $V^k$
> La expresión como formula matematica en la formula $(i)$ no se si es valida para los certamenes de [[INF295 - Inteligencia Artificial|INF295]]. La que si es valida es escribir directamente todas las variables, es decir, si hubieramos tenidos tres vehiculos, la restricción puede escribirse de la siguiente manera:
> $$\sum_{i\in I} V1_{ij} + V2_{ij} + V3_{ij} = 1 ~ ~ \forall j$$
> Lo cual expresa lo mismo que la ecuación (i)




