---
tags:
  - cs/algorithm
---
# General Taxonomy for Problem-Solving Techniques

The problem-solving techniques explained in the course. 

![[Problem-Solving Techniques.svg]]

> [!warning]
> Escribí Trayectory xd en vez de trajectory

> [!question] ¿Cuando usar cada algoritmo?
> Para los problemas, se debe primero realizar algoritmos o técnicas completas, dado que aseguran óptimos (Siempre buscamos la mejor solución). Luego, si el algoritmo no llega a converger en un tiempo deseado, se debe de cambiar a técnicas incompletas para al menos encontrar soluciones optimas locales.
## Exhaustive Search

> See [[Exhaustive Search Algorithms]]

Algorithms that explore the [[Constraint Satisfaction Problem#Search Space|Search Space]] in full. It always gives the best solution, but may be infeasible.
- [[Backtracking]]
- [[Forward Checking]]
- [[Branch and Bound]]
- [[Dynamic Programmig]]

## Local Search

> See [[Local Search Algorithms]]

Algorithms that explore part of the [[Constraint Satisfaction Problem#Search Space|Search Space]], searching for local solutions. It may or not find the best solution, but generally finds local optimum. These are separated based on two types:
- **Constructive**: Algorithm from scratch creates a solution
- **Improvement**: Algorithm that from a complete solution improves it to make it better.

### Trajectory  Search
Focuses on a single solution path
- **Constructive**: [[Greedy Algorithm]], [[Greedy Randomized Adaptive Search Procedure Algorithm]]
- **Improvement**: [[Hill Climbing Algorithm]], [[Simulated Annealing Algorithm]], [[Tabu Search Algorithm]]

### Population Search
Evolves a whole population of candidate solutions
- **Constructive**: [[Ant Colony Optimization]]
- **Improvement**: [[Genetic Algorithm]], [[Particle Swarm Optimization]], [[Harmony Search]]