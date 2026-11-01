---
tags:
aliases:
  - SA
  - Simulated Annealing
---
# Simulated Annealing

Simulated Annealing is a [[Local Search Algorithms|Local Search]] [[Local Search Improvement Algorithms|Improvement Algorithm]] that simulates the process of thermodynamics

Depending on the parameters, SA could lead to the global optimum

## Parameters

Simulated Annealing has the following parameters:
- $T_{in}$: Initial Temperature assigned to the algorithm
- `haltingCriterion`: Critica de parada de búsqueda de puntos con una temperatura $T$
- `terminationCriterion`: Critica de termino del algoritmo. Generalmente cuando la temperatura llega a un punto muy bajo.

> [!seealso] 
> [[How to choose Parameters Values for Local Search Algorithms]]
## Algorithm

The algorithm follows the next steps

> `N(s_c)` is the neighborhood of the point `s_c`

```pseudocode
Procedure simulated-annealing
	(1)
    t ← 0
    initialize T <- T_in
    initialize s_c at random
    initialize s_best ← s_c
    Repeat
        Repeat (2)
            s_n ← select a new point in N(s_c)
            If f(s_n) is better than f(s_c) then
                s_c ← s_n
            Else If random([0, 1]) < e^{\frac{\Delta_{eval}}{T}} then
                s_c ← s_n
			If f_eval(s_c) is better than f_eval(s_best) then
				s_best ← s_c
        Until haltingCriterion()
        (3)
        T ← g(T, t)
        t ← t + 1
    Until terminationCriterion()
EndProcedure
```

1. Initialize the parameters.
	- `t` is the number of iterations
	- `T` is the temperature, starting with the parameter $T_{in}$
	- `s_c` is a variable that stores a point. Starts in a random position.
	- `s_best`: Variable that stores the best point. Starts assigned with the random point `s_c`.
2. Select a new point `s_n`in the neighborhood of `s_c`
	- If the new point is better than `s_c`, then change `s_c` to the new point
	- If not, it can be selected based on a random number between $0$ and $1$. If the random value is less than the [Boltzamn Acceptance Probability](https://en.wikipedia.org/wiki/Boltzmann_distribution) then the solution (even if it's worse) is accepted ($e^{\frac{\Delta_{eval}}{T}}$) ^adf9d9
	- After that, store in `s_best` the best point (compare `s_c` to `s_best`)
	- These will be checked until the halting criteria is done (can be number of iterations per temperature)
3. Modify the temperature
	- The temperature is modified by the function `g(T,t)`, where the temperature changes based on the current temperature `T` and the current iteration `t`-
	- `g(T,t)` generally modifies based on a cooling factor, such as multiplying by a $\alpha$ or decreasing based on a constant `t_c`
	- The cycle ends when the temperature reach a certain point

> [!tip] 
> En el C2 de [[INF295 - Inteligencia Artificial|INF295]] se entrega un arreglo de numeros aleatorios. Estos se utilizan en el [[Simulated Annealing Algorithm#^adf9d9|Segundo paso, selección aleatoria]]

## Observations

> [!tip] 
> Posibles preguntas del C2!

- Simulated annealing does a balance between exploration (_diversificar_) and exploit (_intensificar_). When the temperature is high, is more probable to take worst solutions and explore more regions. When the temperature is low, the probability to explore more regions is so low that the algorithm exploits a region. High temperature ensures that when the temperature finally drops, the algorithm is exploiting the right region (the one closest to the global optimum) rather than a bad one.