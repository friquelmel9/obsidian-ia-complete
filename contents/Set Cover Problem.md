---
tags:
  - cs/optimization
aliases:
  - Set Covering
  - Set Partitioning
  - Set Packing
---
# Set Cover Problem

The Set Cover Problem is an [[Polynomial Complexity|NP]]-hard problem in [[Combinatorial Optimization]]. Given a collection of elements, the set cover problem aims to find the minimum number of sets that incorporate all of these elements

The set covering problem depends on the restrictions for the problem:
- **Set Covering**: At leas every element must be in one subset. Restrictions $\geq$
- **Set Partitioning**: Each element must be on one subset. Restrictions $=$
- **Set Packing**: Each element is in at most one subset. Restrictions $\leq$

![[Set Covering - Partitioning - Packing.png]]
## CSP Model

A Set Cover Problem can be modeled as an [[Constraint Satisfaction Problem|CSP/CSOP]].

- **Variables:** 
	- $x_i$: The available set is choosen
- **Domain:**
	- It's choosen or not. $D_{x_i} = \{1,0\}$
- **Constraint:**
	- Coverage: Each coverage constraint includes the elements that the set contains. Depending on the type, the operator changes between $\leq, =$ or $\geq$.

The objective function can be set if choosing some set has consequences, like monetary incentives or human cost.
