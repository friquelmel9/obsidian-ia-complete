---
tags:
  - cs/optimization
aliases:
---
# Job-Shop Scheduling Problem

In a general job scheduling problem, we are given $n$ jobs $J_1, J_2, ..., J_n$ of varying processing times, which need to be scheduled on $m$ machines with varying processing power, while trying to minimize the makespan. 

In the Job-Shop specific problem, each job has also a set of operations $O_{i1},O_{i2},\cdots,O_{im}$, which have to be done in a specific order. We also have machines $W_1, W_2, \cdots, W_k$, which can have operations exclusive to the machine

# Model

A Job-Shop Scheduling Problem can be modeled as an [[Constraint Satisfaction Problem|CSP/CSOP]]

- **Variables**:
	- $x_{ij}$: The starting time of the operation $O_j$ for the job $J_i$
- **Domains**
	- $D_{x_{ij}}$: $0$ to $C_{max}$, where $c_{max}$ is the maximum time for all the jobs. 
- **Parameters**
	- $t_{ij}$: Estimated time for the operation $j$, work $i$
	- $M_{ij}$: Machine needed for the operation $j$, work $i$
- **Restrictions**
	- The next operations must be done after the estimated time of the previous is done $$x_{ij} + p_{ij} \leq x_{i(j+1)}$$
	- The operation

