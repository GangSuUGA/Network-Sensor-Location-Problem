## References Link: 
 - Tutorial of [**Mixed-integer Programming: A Guide to Computational Decision-making**](https://www.toptal.com/algorithms/mixed-integer-programming) by Shanglun Wang
 - [**Applied Mathematical Programming**](http://web.mit.edu/15.053/www/AMP.htm) by Bradley, Hax, and Magnanti (Addison-Wesley, 1977)
 - [**Matlab Code**](https://www.mathworks.com/help/optim/ug/intlinprog.html)
_______________________________________________________________________

## Mathematical Form:   
**Objective**:	  Minimize cT x                 
**Constraints**:	 
- A x = b (linear constraints)                  
- l ≤ x ≤ u (bound constraints)                 
- some or all xj must take integer values (integrality constraints)              
________________________________________________________________________

To make integer programming possible, several mathematical algorithms are used. 
If you are interested in the underlying algorithms, I recommend studying the cutting-planes algorithm and the branch-and-bound algorithm 
[**here**](http://web.mit.edu/15.053/www/AMP-Chapter-09.pdf).     

## Cutting-Planes Algorithm: 

## Branch-and-Bound Algorithm: 

## Example:  
Here is an example in tutorial that use **Branch-and-Cut** via PuLP (a popular operations research modeling library for Python). 
You can find information about [**PuLP here**](https://github.com/coin-or/pulp). 

```
import pulp as pl

# declare some variables
# each variable is a binary variable that is either 0 or 1
# 1 means the item will go into the knapsack
a = pl.LpVariable("a", 0, 1, pl.LpInteger)
b = pl.LpVariable("b", 0, 1, pl.LpInteger)
c = pl.LpVariable("c", 0, 1, pl.LpInteger)
d = pl.LpVariable("d", 0, 1, pl.LpInteger)

# define the problem
prob = pl.LpProblem("knapsack", pl.LpMaximize)

# objective function - maximize value of objects in knapsack
prob += 5 * a + 7 * b + 2 * c + 10 * d

# constraint - weight of objects cannot exceed 15
prob += 2 * a + 4 * b + 7 * c + 10 * d <= 15

status = prob.solve()  # solve using the default solver, which is cbc
print(pl.LpStatus[status])  # print the human-readable status

# print the values
print("a", pl.value(a))
print("b", pl.value(b))
print("c", pl.value(c))
print("d", pl.value(d))
```

