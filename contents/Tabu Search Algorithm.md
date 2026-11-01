---
tags:
aliases:
  - TS
  - Tabu Search
---
# Tabu Search

Tabu Search is a [[Local Search Algorithms|Local Search]] [[Local Search Improvement Algorithms|Improvement Algorithm]] where we search solutions

## Parameters

The only parameter exclusive to Tabu Search is the max size (`MAX_TS`), which depends on the implementation of the algorithm (specially the `terminationCriterion()`, which indicates when to halt the algorithm)

- Tabu List could have a maximum size. If the max size is reached, then the first neighbor to enter the list is removed in a queue fashion ([[First In First Out|FIFO]])

Other parameters can be number of iterations `t` or `max_time`.
## Algorithm

> `N(s_c)` is the neighborhood of the point `s_c`

```pseudocde
Procedure tabu search
	(1)
    initialize s_c at random
    initialize tabu_list as empty
    initialize s_best ← s_c
    Repeat (2)
        s_v ← select from N(s_c) the best non tabu point
        s_c ← s_v
        update tabu_list
        If f(s_c) is better than f(s_best) then
            s_best ← s_c
    Until terminationCriterion()
EndProcedure
```

1.  Initialize the variables
	- `s_c` is a variable that stores the current point. Starts at random
	- `tabu_list` is a list [[First In First Out|FIFO]] (Or queue) that stores the visited parameters.
	- `s_best` stores the current best point. Is assigned `s_c` in the start
2. Search the neighborhoods.
	- `s_v` stores the best neighbor from the neighborhood that is not on `tabu_list`
	- `tabu_list` is updated with the new point
	- If `s_c <- s-v` is better than `s_best`, `s_best` modifies it value to the new optimum.
	- This goes until the terminationCriterion is reached (generally number of iterations of max_time execution)
	- Here can be implemented the logic of maximum tabu list size.

## Iteration Example

Consider the following [[Knapsack Problem]] where...

$$
\begin{aligned}
f = \max \quad & 18 \cdot x_1 + 25 \cdot x_2 + 11 \cdot x_3 + 14 \cdot x_4 \\
\text{condition:} \quad & 2 \cdot x_1 + 2 \cdot x_2 + x_3 + x_4 \le 3 \\
\text{variables:} \quad& x_1, x_2, x_3, x_4 \in \{0, 1\}
\end{aligned}
$$

- The `terminationCriterion` is to stop after 5 iterations
- The `tabu_list` maximum size is 2
- The movement function is a shift from $0$ to $1$
- Only factible solutions are available.

| it  | `s_c`        | `s_best` | `N(s_c)`                                             | `tabu_list` | mov. tabú |
| :-: | :----------- | :------- | :--------------------------------------------------- | :---------: | :-------: |
|  1  | 1000(18)     | 1000(18) | 0000(18)<br>~~1100(43)~~<br>1010(29)<br>1001(32)     |    `{}`     |    j4     |
|  2  | 100**1**(32) | 1001(32) | 0001(14)<br>~~1101(57)~~<br>~~1011(43)~~<br>1000(18) |   `{j4}`    |    j1     |
|  3  | **0**001(14) | 1001(32) | 1001(14)<br>0101(39)<br>0011(25)<br>0000(0)          |  `{j4,j1}`  |    j2     |
|  4  | 0**1**01(39) | 0101(39) | 1101(57)<br>0001(14)<br>~~0111(50)~~<br>0100(25)     |  `{j1,j2}`  |    j4     |
|  5  | 01**0**0(25) | 0101(39) | ~~1100(43)~~<br>0000(0)<br>0110(36)<br>0101(39)      |  `{j2,j4}`  |    j3     |
|  6  | 01**1**0(36) | 0101(39) | —                                                    |  `{j4,j3}`  |     —     |
