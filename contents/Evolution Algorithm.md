---
tags:
aliases:
---
# Evolution Algorithms

Evolution Algorithms are the implementation of [[Genetic Algorithm]] for [[Constraint Satisfaction Problem|CSP/CSOP]]. It simulates the concept of [Natural Selection](https://en.wikipedia.org/wiki/Natural_selection). With a initial population, enough mutation and crossing, the solution will converge to optimums.

## Concepts

- **Individual**: Represents a solution of the problem
- **Population** A set of individuals
- **Generation**: Indicates the time order of the population grown from mutations and crossing.
- **Fitness**: Indicates the quality of a individual (is the term for the evaluation function in evolution algorithms)
- **Selection**: Indicates the probability or chance that some individuals cross with each other in some generation. A bad individual (based on the fitness function) may have less (or null) probability of crossing.
- **Elitism**: Indicates the probability that some individuals may live through the next generation.

> [!info] Ruleta
> La ruleta esta relacionada con el elitismo y la selección. Se da cierta probabilidad a cada individuo según su evaluación. Un ejemplo es utilizando la probabilidad sobre la suma total de las evaluaciones (fitness)
> ![[Ruleta.svg]]
> Notar que incluso el individuo con peor evaluación pertenece a la ruleta. Esto es porque puede que este individuo tenga algún gen particular que pueda potenciar a la especie a largo plazo.
## Parameters

Evolution algorithms have a lot of parameters:
- **Population Size** `n`: Indicates the number of individuals in a population
- **Probabilities**:
	- $P_{mut}$: Probability of a mutation occurring
	- $P_{crossing}$: Probability of a crossing 
- **Number of generations**: Indicates how many generations to do

> [!tip] Parameter selection
> In general, the population and the number of generations are better tuning, while the probabilities are better being controlled (this is exactly elitism) (see [[How to choose Parameters Values for Local Search Algorithms]])

The mutation and crossing functions must be implemented based on the problem.
## Algorithm

The algorithm generally does the following:

1. Generate initial population
	- Each individual can be made randomly, by [[Greedy Algorithm|Greedy]] or anyway
2. Start the Generation procedure
	- In each generation, each individual from the population is evaluated (using the fitness function)
	- (**Selection**) Depending on the probability, the new individuals may be born from a mutation or a crossing. 
	- (**Elitism**): Form the new generation using the newborns, optionally injecting the elite individuals directly from the previous generation
	- These depends on the parameters selected previously
3. Iterate through generations until convergence is applied or the max number of generations is reached.

![[Evolution Algorithm.svg]]