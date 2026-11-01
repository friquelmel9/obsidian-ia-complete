---
tags:
aliases:
  - Greedy
---
# Greedy Algorithm

A greedy algorithm is a simple, intuitive algorithmic paradigm that builds up a solution step-by-step, making the locally optimal choice at each stage with the hope of eventually reaching the global optimum.

It need's the following definitions:
- **Representation**
- **Evaluation Function**
- **Myopic Function**: It tell's the next step to build the solution based on the current state of the solution (it doesn't considerate future states)
- **Initial Solution**: Null, an empty solution to start working from

> [[Greedy Randomized Adaptive Search Procedure Algorithm|GRASP]] is a variant of Greedy with Probability.

![[VRP-GreedyExample.svg]]

> Example of Greedy in a [[Vehicle Routing Problem|VRP]]. The solution provided by it is $=440$, but is not the global optimum. (An improved solution is A->B->E->D->C, with total $=200$).
> This uses:
> - **Representation**: A valid tour
> - **Evaluation Function**: The cost of the tour
> - **Myopic Function**: Path with minimum value from last node visited.