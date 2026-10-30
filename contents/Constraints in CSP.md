---
tags:
  - cs/optimization
aliases:
  - Constraint in CSP/CSOP
---
# Constraints in CSP/CSOP

There are types of constraints depending on various conditinos

## Variable Types

Depending on the number of variables in the restriction, the constraint can be:
- **Unary**: Includes only one variable. E.g $x_1 = 2$
- **Binary**: Includes two variables. E.g $x_1 \neq x_2$
- **Tertiary** Includes three variables. E.g $x_1 + x_2 \neq x_3$

And so on

## Hardness

### Hard Constraint

A Hard Constraint is a type of constraint that **must** be accomplished for the CSP to be considered correct. Violating any constraint makes the solution invalid (Infeasible)

[[Constraint Satisfaction Problem|CSP]] are made of only hard constraints.

### Soft Constraint

A soft constraint is a type of constrait that supports the objective function for a problem, but when violating the constraint doesn't make the solution invalid.

This correlates to the objective function, so soft constraints can only be found on [[Constraint Satisfaction Problem|CSOP]]

> [!info] 
> En general, en español, se considera a la restricción suave como "relajación". Se define que se puede "relajar" el problema.