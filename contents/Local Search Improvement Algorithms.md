---
tags:
aliases:
  - Improvement Algorithm
  - Improvement Algorithms
---
# Improvement Algorithms

Improvement Algorithms is a type of [[Local Search Algorithms]] where a solution is improved from an initial one

![[HS+SA+TS.svg]]

> In the image, blue solutions are solutions better than the original, while red ones are the best one among the neighborhood of $x$. The dotted circle is the neighborhood of $x$.

Some algorithms that are Local Search Improvement are:
- [[Hill Climbing Algorithm|Hill Climbing]]: Start from a initial solution and improve it to the optimum
- [[Simulated Annealing Algorithm|Simulated Annealing]]: Simulates thermodynamics to find the optimum
- [[Tabu Search Algorithm]]: Exploration with short-memory

## Requirements

- **Representation**: The representation of the problem. 
- **Initial Solution**: Initial solution to improve. Generally given by randomness or [[Greedy Algorithm|Greedy]].
	- The initial solution gives the neighborhood.
- **Movement Function** $f_{mov}(x)$: It takes a current solution ($x$) and applies a small, defined modification to produce a neighboring solution ($x'$).

## Concepts

- **Neighbor** ($x'$): A solution next to the current solution. A solution is "next" to the current one if it can be given by the $f_{mov}(x)$ (**Movement Function**)
- **Neighborhood**: All the posible neighbors from the current solution

## Movement Options

The movement function can be implemented in various ways. However they fall in the next categories:
- **Swap**: Exchange values between variables.
- **Shift**: Modify the value of a variable based on the domain.

> [!warning] Selección del movimiento según problema
> Las funciones de movimiento deben de asignarse bien respecto al problema. Una opción de movimiento incorrecta puede llevar a soluciones de mala calidad o no investigar correctamente la solución.
> 
> Por ejemplo, imaginemos un [[Knapsack Problem|Knapsack]] con representación binaria (0 es no llevar, 1 es llevar) con tres objetos. Si la solución inicial es `[0,1,0]`, utilizar un movimiento del tipo **Swap** nos dara unicamente soluciones donde se lleve un objeto (El vecindario seria `[1,0,0]` y `[0,0,1]`), sin explorar otras soluciones donde se podria agregar otro objeto más.
> 
> Una forma de solucionarlo es extender el arreglo más lejos de donde tenga validez. Es decir, para tres objetos se podría tener un arreglo de la forma `[0,1,0|0,1,1,0]`. El swap se hace entre todos los valores, pero unicamente los tres primeros se consideran solución. De esta manera se agregan otras posibilidades en el vecindario manteniendo la implementación de swap. En general este enfoque es *horrible*, es mejor agregar simplemente el shift+swap.

## Observations