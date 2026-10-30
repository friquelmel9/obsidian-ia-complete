---
tags:
  - cs/optimization
aliases:
---
# Quadratic Assignment Problem

There are a set of $n$ facilities and a set of $n$ locations. There's a distance between all locations and a weight associated with each pair of facilities. The problem is to assign the facilities in the locations minimizing (or maximing) the weight [^1]

![[QAP.png]]
## Model

The problem can be modeled as an [[Constraint Satisfaction Problem|CSOP]]

- **Variables**: with $i \in \{1,\cdots,N\} = I$ and $j\in\{1,\cdots,N\} = J$
	- $x_{ij}$: Indicates if the facility $i$ is put on the location $j$
- **Domain**
	- $D_{x_{ij}}$: Binary Decision $\{1,0\}$
- **Parameters**: With $i,k \in I$ and $j,l \in J$
	- $N$: The number of facilities and locations
	- $d_{jl}$: Distance between locations $j$ and $l$.
	- $f_{ik}$: Weight associated between a pair of facilities $i$ and $k$
- **Constraints**:
	- The facility must be on one location $$\sum_{j \in I} x_{ij} = 1 ~ ~ \forall i$$
	- Each location must have one facility $$\sum_{i \in I}x_{ij} = 1 ~ ~ \forall j$$

The objective function must work to minimize the distance between two facilites that have a lot of weight. This is to make them more valuable if they are near each other. 
This is considered the **Quadratic Routing Cost**
$$\min f = \sum_{i\in I}\sum_{k\in I}\sum_{j \in J}\sum_{l \in J} d_{jl} \times f_{ik} \times x_{ij} \times x_{kl} $$

[^1]: Definition from https://en.wikipedia.org/wiki/Quadratic_assignment_problem
