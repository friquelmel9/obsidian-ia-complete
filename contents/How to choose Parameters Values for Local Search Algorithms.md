---
tags:
aliases:
---
# How to choose Parameters Values for Local Search Algorithms

A lot of [[Local Search Algorithms]] have a lot of parameters that could affect the quality of the solutions or the time it converges to one. For example...

- [[Hill Climbing Algorithm|HC]] has the number of `RESTARTS`
- [[Simulated Annealing Algorithm|SA]] has the start temperature, the function `g` that modifies the temperature, etc.
- [[Tabu Search Algorithm|TS]] has the size of the tabu list.
- [[Evolution Algorithm]] has the population size $n$, the probability of mutation and crossing, and number of iterations.

For these, the parameters can be selected in two ways:
- **Tuning** (_Tunear_): Parameters are selected beforehand
- **Monitoring** (_Controlar_): Parameters are changed in execution, based on the current state of the solution.

> [!info] Tuning Libraries
> Hay un montón de formar de tunear. Generalmente se hace manualmente para casos pequeños pero también se tienen librerias que permiten ver que parámetros pueden funcionar.
> Algunas librerias son ¿Race, Evoca y paramILS (paramILS es la más apoyada por la profe)

