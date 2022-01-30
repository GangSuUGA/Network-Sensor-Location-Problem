## References Link: 
 - Tutorial of [**Mixed-integer Programming: A Guide to Computational Decision-making**](https://www.toptal.com/algorithms/mixed-integer-programming) by Shanglun Wang
 - [**PuLP**](https://coin-or.github.io/pulp/index.html) 
 - [**Applied Mathematical Programming**](http://web.mit.edu/15.053/www/AMP.htm) by Bradley, Hax, and Magnanti (Addison-Wesley, 1977)
 - [**Matlab Code**](https://www.mathworks.com/help/optim/ug/intlinprog.html)
 - Parganiha, Kanishka. “[**LINEAR PROGRAMMING WITH PYTHON AND PULP**](https://iaeme.com/MasterAdmin/Journal_uploads/IJIERD/VOLUME_9_ISSUE_3/IJIERD_09_03_001.pdf).” (2018).
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
Here is an example in tutorial of PuLP (a popular operations research modeling library for Python). 
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

## Another example:
![image](https://user-images.githubusercontent.com/88390140/132880710-849086bf-274c-4057-867f-9ebcc0f77e61.png)     
![image](https://user-images.githubusercontent.com/88390140/132880764-f1e62441-8db1-4a01-8b19-288f469412da.png)    
![image](https://user-images.githubusercontent.com/88390140/132880780-3df12d87-b8fe-406d-b464-3a48552d69fd.png)     
![image](https://user-images.githubusercontent.com/88390140/132880798-fb1c7000-6fa0-4d71-b379-0d635cd6d4f2.png)    
![image](https://user-images.githubusercontent.com/88390140/132880816-8c7b7571-5d2e-4da3-8e6d-3c47bafb0881.png)     
![image](https://user-images.githubusercontent.com/88390140/132880844-67e5c154-dd1e-4d6a-a995-b88bb3c606f7.png)   
![image](https://user-images.githubusercontent.com/88390140/132880910-a6e89716-7de5-44fa-b08c-375f9abf881b.png)
![image](https://user-images.githubusercontent.com/88390140/132881052-06e126c9-341a-439d-a974-31f490ed0ef4.png)
![image](https://user-images.githubusercontent.com/88390140/132577261-ba13c7a3-e395-480b-824c-6bf27820fa6f.png)

