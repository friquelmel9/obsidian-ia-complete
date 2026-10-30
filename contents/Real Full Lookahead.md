---
tags:
  - cs/optimization
aliases:
---
# Real Full Lookahead

Real Full Lookahead checking algorithm is a look-ahead algorithm to solve [[Constraint Satisfaction Problem|CSP]] problems.

It's similar to [[Forward Checking]] algorithm, but instead of checking the domain of the variables connected through the current one, it checks all the other variables. In practice, this technique is too expensive to be used.