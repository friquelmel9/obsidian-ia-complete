---
tags:
  - cs/optimization
aliases:
---
# Knapsack Problem 

Given a maximum weight and a set of objects (each one with a value and a weight), search for a combination that maximizies the value (or quantity)

## Model

The Knapsack problem can be model as an [[Constraint Satisfaction Problem|CSOP]]

- **Variables**: 
	- $x_i$: Take the object $i$
- **Domain:**
	- $D_{x_i}$: Take or don't take $\{0,1\}$
- **Parameters**:
	- $V_i$: Value for object $i$
	- $W_i$: Weight for object $i$
	- $M$: Max weight
- **Constraints**
	- Weight of the objects less than the max capacity. $$\sum W_i~x_i  \leq M$$

The objective function for the [[Constraint Satisfaction Problem|CSOP]] depends on the problem
- Max quantity of objects $$\max f = \sum x_i$$
- Maximize Value $$\max f = \sum V_i~x_i$$
