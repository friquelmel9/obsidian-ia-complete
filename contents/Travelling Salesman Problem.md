---
tags:
  - cs/optimization
aliases:
  - TSP
---
# Travelling Salesman Problem

Given a list of cities and the distances between each pair of cities, what is the shortest possible route that visits each city exactly once and returns to the origin city?

![[TSP.png]]
## Model

This problem can be modeled as an [[Constraint Satisfaction Problem|CSOP]]

- **Variables**:
	- $x_{ijk}$: If travels from city $i$ to city $j$ in step $k$
- **Domains**:
	- $x_{ijk}$: Binary value $\{0,1\}$
- **Parameters**
	- $c_{ij}$: Cost for the city $i$ to $j$
- **Constraints**
	- For each city $j$, it must come from a city $i$ $$\sum_{i\neq j}\sum_{k} x_{ijk} = 1 ~ ~ \forall j$$
	- For each city $i$, it must go to a city $j$ $$\sum_{j\neq i}\sum_{k} x_{ijk} = 1 ~ ~ \forall i$$
	- Must travel once in each step $k$ $$\sum_{i}\sum_{i \neq j} x_{ijk} = 1 ~ ~ \forall k$$
	- The current travel must start from the previous one. $$\sum_{i\neq j}x_{ijk} = \sum_{r\neq j}x_{jr(k+1)} ~ ~ \forall j,k$$
