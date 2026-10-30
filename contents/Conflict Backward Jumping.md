---
tags:
  - cs/optimization
  - cs/algorithm
aliases:
  - CBJ
---
# Conflict Backward Jumping

Conflict Backwad Jumping is an algorithm to solve [[Constraint Satisfaction Problem|CSP/CSOP]] based on [[Backtracking]]. 

Instead of backtracking to the previous instanciated value, the backtracking goes to the last instanced variable that has conflict with the current variable. We need to compare all the assigments that failed, and take the first instanciaded variable on the assigment. Then, with a list of all the first conflict in each of the instances, we take the last instanced one from the list.

## Example

In the next image, CBJ jumps to $B$. The $E$ variable has two possible assigments:
- $E=R$: Conflict with $A$
- $E =G$: Conflict with $B$ and $C$. Take the first one to be instanced (Also expressed as a $\min$), being $B$.
After we have all the first conflicts, being $A$ and $B$, we take the last instanced one (Also expressed as a $\max$), being $B$. 

![[Backtracking vs GBJ vs CBJ.png]]