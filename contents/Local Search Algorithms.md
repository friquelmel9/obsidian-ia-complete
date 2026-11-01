---
tags:
  - cs/algorithm
aliases:
  - Local Search
  - Búsqueda Local
---


# Local Search Algorithms

A local search algorithm is a kind of algorithm where it obtains solutions based on searches from limited regions from the [[Constraint Satisfaction Problem#Search Space|Search Space]]. It generally doesn't find the most optimal solutions, but it can find optimals in less time than [[Exhaustive Search Algorithms]], but the solutions are poorer compared to exhaustive.

![[Search Space Local Search.svg]]

Each space with lines is considered a region. Each region has an optimal solution in them called $S'_i$. The solution given by the local search algorithm will be the max value of the regions it explored.

In Local search, there are two kinds of concepts when referring to solutions in the Search Space.
- **Exploit** (_Explotar, Intensificar_): Is to improve or search for better solutions in the current [[Constraint Satisfaction Problem#Search Space|Search Space]] 
- **Explore** (_Explorar, diversificar_): Leave the current region of the Search space to another one in search of a better optimum

## Types

There are two types of algorithms depending on how they make the solution

### Constructive 
Algorithm from scratch creates a solution

Constructive algorithms are:
- [[Greedy Algorithm]]
- [[Greedy Randomized Adaptive Search Procedure Algorithm]]

### Improvement
Algorithm from initial solution improves it.

Improvement algorithms are:
- [[Hill Climbing Algorithm]]
- [[Simulated Annealing Algorithm]]
- [[Tabu Search Algorithm]]: Search all neighborhood and moves to the best neightbor, making use of a Tabú List 

> Further explanation: [[Local Search Improvement Algorithms|Improvement Algorithm]]
### Population

Algorithm from initial solutions makes generations until a solution converges between the individuals. Based on the concept of [Natural Selection from Charles Darwin](https://en.wikipedia.org/wiki/Natural_selection)

Population-based algorithms are:
- [[Ant Colony Optimization]]
- [[Genetic Algorithm]]
- [[Evolution Algorithm]]
## Functions and Constant Concepts

Local Search algorithms needs from the following to work properly:

i. **Representation**: The representation is the way the algorithm understands the solution
- Example: In a [[Travelling Salesman Problem|TSP]] a representation can be a vector with the clients order. $[1, 4, 2, ...]$
- The representation can be valid, invalid, complete, incomplete.

ii. **Evaluation Function** $( f_{eval}(x) )$ : Takes a candidate solution $x$ as input and assigns it a numerical score representing how "good" or "optimal" it is.
- It determines the _quality_ of the solution

> [!caution] 
> The Evaluation Function is **not** the same as the objective function. They are correlated, because the evaluation function tries to converge to an optimum value from the objective function, but it may have extra parameters, such as Temperature.

iii. **Initial Solution(s)**: An initial solution to work from
- Generally is done randomly or with [[Greedy Algorithm|Greedy]]
- Technically, in Constructive algorithms the initial solution is a null solution (empty).

iv. **Parameters**: Common constants used in problems. Examples are:
- Iterations: Max number of iterations for the algorithm.
- RE-START: Select how many times an algorithm can start from a new initial solution.(Improvement Algorithms)
- There can be specific parameters for specific algorithms, such as $TS$ (Tabu size) for the [[Tabu Search Algorithm]]

> [!seealso] 
> Parameters can be selected before or changed during execution. Diferent parameters may change the quality of the solution. See [[How to choose Parameters Values for Local Search Algorithms]]

The next ones are used in only one type of algorithm:

- **Myopic Function** $f_{miope}(x)$: Makes decisions based _only_ on immediate, local information without considering long-term consequences.
	- Used in Constructive Algorithms such as [[Greedy Algorithm|Greedy]]

- **Movement Function** $f_{mov}(x)$: It takes a current solution ($x$) and applies a small, defined modification to produce a neighboring solution ($x'$).
	- Used in Improvement Algorithms such as [[Hill Climbing Algorithm|HC]]
	- There are variants depending on which neighbor I take. There First-Improvement (_Primera Mejora_) or Best-Improvement (_Mejor Mejora_)
