---
tags:
  - cs/ai
aliases:
  - CSP/CSOP
  - CSP
  - CSOP
  - COP
---
# Constraint Satisfaction Problem

 A constraint satisfaction problem is defined as having the following:
 - $X = \{X_1,X_2,\cdots,X_n\}$: Set of variables
 - $D = \{D_{X_1}, D_{X_2},\cdots,D_{X_n}\}$: The Domain for each variable
 - $C = \{C_1,C_2,\cdots,C_m\}$: The Constraints of the problem

A problem is optimized (CSOP) if it's given an objective function
- $f$: Objective function

> [!tip] 
> Las variables siempre son que es lo que quiero obtener como respuesta al modelar.

The objective for CSP/CSOP are different
- **CSP**: Find one (or more) ==valid== solution(s)
- **CSOP**: Find one (or more) ==optimal== solution(s)

## Search Space

> [!note] 
> En español conocido como Espacio de Búsqueda (EB)

The search space corresponds to all the possible values for the CSP problem. 

If the problem has a total of $n$ variables, each one with a total of $m$ possible values, then the search space is $m^n$

![[Search Space.png]]

> [!example] Search Space with two variables with different domains
> If we have a model that has two variables $x_i$ and $y_j$, where $i \in \{1,\cdots,n\}$ and $j \in \{1, \cdots, m\}$

> [!tip] Minimize the Search Space
> The search space grows exponentially compared to the number of variables. It's best practice to have a bigger domain that a bigger number of variables.
> Generally speaking, variables in the form of $x_{ij}$, $x_{ijk}$ and so on are not the best practice, due to it's growth in the Search Space because of the number of variables.

## Assignment Types

An assignment for an variable has various types:

Depending on constraints:
- **Consistent Assignment**: An assignment that does not break any constraint

Depending in the total of variables
- **Partial Assignment**: An set of assignment 
- **Complete Assignment**: All variables are assigned

**==The solution of a CSP/CSOP is a consistent and complete assignment of variables==**
