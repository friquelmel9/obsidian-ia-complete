---
tags:
  - cs/algorithm
  - cs/optimization
aliases:
  - GBJ
---
# Graph Backward Jumping

Graph Backwad Jumping is an algorithm to solve [[Constraint Satisfaction Problem|CSP/CSOP]] based on [[Backtracking]]. 

Instead of backtracking to the previous instanciated value, the backtracking goes to the last instanciated variable connected with the current issue.

## Example

In the next image, GBJ goes to $C$. $E$ (The node with conflicts) it's connected to $A,B$, and $C$. Because the variable order is alphabetically, then the last instanced is $C$.

![[Backtracking vs GBJ vs CBJ.png]]