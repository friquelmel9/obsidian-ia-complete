---
tags:
  - cs/optimization
aliases:
---
# Airline Crew Scheduling

The Airline Crew Scheduling is a type of [[Crew Scheduling Problem]]

The plan is to have a flight start in one position and end in the same position after a number of travels

## CSP Model

Airline Crew Scheduling can be represented as a [[Constraint Satisfaction Problem|CSP/CSOP]].
- **Variables:** 
	- $x_{ij}$: The pairing $j$ covers the flight $i$
- **Domain**: 
	- Binary, covers or not $D_{x_{ij}} = \{1,0\}$
- **Constraints**:
	- If a flight is covered $0$ times, the plane doesn't fly
	- Each flight must be assigned to one crew (meaning a [[Set Cover Problem|Set Partitioning]]) $$\sum_{J} ~ x_{ij} = 1 ~~~~ \forall ~ I$$
	- Each flight must go back to the starting place. #to-do 

The objective function can be represent as cost for the pairing $j$ and flight $i$.

![[Airline Crew Scheduling.png]]
## Optimization

This problem can be solved with optimization using [[Column Generation Model]]. 

In the previous image, corresponds to the valid sets of flights. Then the model changes to this:

- **Variables**: With $i \in \{1,\cdots,n\}$, with $n$ the number of sets
	- $T_i$: The valid set $i$ is made
- **Domain**: 
	- $D_{T_i}$: Binary decision $\{1,0\}$
- **Constraints**:
	- Each flight must be made once. This means means that, for each flight (for example , $101$), a constraint is made where it includes each set that includes the flight,
	- Example: For flight $101$, the restricction would look like $x_{1} + x_{2} + x_{3} = 1$.

The Objective functions would be based on the tours. For example, if minimizing the number of tours:
$$\min f = \sum_{i=0}^n T_i$$