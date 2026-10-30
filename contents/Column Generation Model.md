---
tags:
  - cs/optimization
aliases:
---
# Column Generation Model

A column generation model is a way to modeling [[Combinatorial Optimization|Combinatorial Problems]], converting the problem into a [[Set Cover Problem]], specifically, a [[Set Cover Problem|Set Partitioning]]

1. For any [[Constraint Satisfaction Problem|CSP/CSOP]], write all the posible complete assignments.
2. Transform the problem [[Set Cover Problem|Set Partitioning]], where each possible assignment is a variable.
	- The Set Partitioning is not obligatory, it can be any other problem, but is the most common case for Column Generation Model. [^1]
3. Assure the constraints of the original problem are also in the new problem
	- This can be assured by building new constraints, or only taking the complete assigments that are consistent. [^2]


## Examples

Common examples are:
- [[Airline Crew Scheduling Problem#Optimization]]: Write any set of possible travels.

[^1]: Realmente no se si es el caso más común, sin embargo, es el unico que se vio en el curso de [[INF295 - Inteligencia Artificial]]

[^2]: See [[Constraint Satisfaction Problem#Assignment Types|CSP > Assignment Types]] for the definitions 
