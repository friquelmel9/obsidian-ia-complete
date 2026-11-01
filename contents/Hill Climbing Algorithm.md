---
tags:
aliases:
  - HC
  - Hill Climbing
---
# Hill Climbing Algorithm

Hill Climbing is an iterative [[Local Search Algorithms|Local Search]] Improvement Algorithm. It improves a solution to find the local optimum 

![[HC.svg]]

## Parameters

The hill climbing algorithm has the following parameters:
- $RESTARTS$: Number of restarts done by the algorithm
## Variants

- **First-Improvement** (_Primera Mejora_): HC jumps to the first neighbor that improves the current solution
- **Best_Improvement** (_Mejor Mejora_): HC searches the whole neighborhood and jumps to the neighbor that has the best improvement 
## Algorithm

> Assume the $f_{eval}(x)$ returns the next neighbor with better evaluation (even if is _MM_ or _PM_)

```pseudocode
Procedure hill-climbing
	local <- FALSE
	s_c <- select-random-point
	Repeat
		s_n <- f_eval(s_c)
		if f_eval(s_n) better than f_eval(s_c):
			s_c <- s_n
		else:
			local <- TRUE
	Until local
```

