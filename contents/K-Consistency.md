---
tags:
  - cs/optimization
aliases:
---
# $K$-Consistency

A [[Constraint Satisfaction Problem|CSP/CSOP]] is $k$ consistent if, for any set of $k-1$ variables and for any consistent assignment [^1] to those variables, a consistent value can be assigned to any $k$-th variable. [^2]

> [!example] 
> A $1$-Consistency means that, given the empty set, we can assign at least one of the variables to be consistent. 

There are cases to make the consistency:
- 1-Consistency is [[Node Consistency|Node-Consistent]]
- 2-Consistency is [[Arc Consistency|Arc-Consistent]]
- 3-Consistency is [[Path Consistency|Path Consistent]]

> [!important] 
> If I have $N$ consistency with $N$ variables, then the problem has a solution. Checking if it has a solution with this method is bad because of the high cost of calculating the $k$ consistency.
## Strong $K$-Consistency

A [[Constraint Satisfaction Problem|CSP/CSOP]] is strongly $K$ consistent if it is $k$-consistent from $k$ to $1$. That means, is $1$ consistent, $2$ consistent, and so on till $k$ consistency. 

> [!algorithm] Complexity of $n$ consistency
> The complexity of $n$ consistency is, at worst, $O(x^n)$.

[^1]: See [[Constraint Satisfaction Problem#Assignment Types|CSP > Assignment Types]]

[^2]: Source is from [[Artificial Intelligence - A modern Approach]] textbook, page 172
