---
tags:
  - cs/optimization
aliases:
  - FC
---
# Forward Checking

Forward checking algorithm is a look-ahead algorithm to solve [[Constraint Satisfaction Problem|CSP]] problems.

When a variable is assigned a value, we check all the domains of the variables that are connected to the current one. 
- If the current value assigned is in a domain of one of the connected variables, then we take that value out of the domains. 
- If a variable runs out of values (meaning a null domain), then we know the current branch is non-viable (Refers to [[Trashing]]). Return to other value

This technique can complement [[Backtracking]], [[Graph Backward Jumping|GBJ]] and [[Conflict Backward Jumping|CBJ]].

> [!warning] Tipo de técnica
> Incluso si FC filtra el dominio de las variables, esta es una estrategia de resolución, no de filtro. Esto es porque la técnica se hace en tiempo de ejecución, mientras se resuelve el problema, a diferencia de técnicas como [[Arc Consistency Algorithm 3|AC3]] en donde se realiza previo a la solución.

