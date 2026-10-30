---
tags:
  - cs/optimization
aliases:
---
# Trashing

Trashing are instances of an [[Constraint Satisfaction Problem|CSP/CSOP]] problem that are invalid because of the constraints. The problem with trashing is that the algorithm will still search the tree, even if the solution is already invalid because of certain assigned values.

They add to the [[Constraint Satisfaction Problem#Search Space|Search Space]] while not being useful to the problem solution. 

We can reduce trashing by using methods such as [[Heuristic Algorithms]]