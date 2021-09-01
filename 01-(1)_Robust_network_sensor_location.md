#### Paper Link:
#### Xu, Xiangdong et al. “Robust network sensor location for complete link flow observability under uncertainty.” Transportation Research Part B-methodological 88 (2016): 1-20. https://www.sciencedirect.com/science/article/pii/S0191261516000436?via%3Dihub
___________________________________________________________________________________________________________________________________________________________________________________

In this paper, the author provide a **robust** network sensor location model for complete link flow inference via a node-based approach while **considering the propagation of measurement errors**. 

## Example 
![image](https://user-images.githubusercontent.com/88390140/131688472-dd5b92ce-fc45-43ee-9995-13fa6260309e.png)
![image](https://user-images.githubusercontent.com/88390140/131688506-5317b33f-ab86-4050-9c83-2bd9bb9a9e46.png)
The flow variance on unobserved link a can be expressed as: 
![image](https://user-images.githubusercontent.com/88390140/131688630-5bd64c1b-63bd-49e8-8220-bec325ace1aa.png)
a: unobersed link; b: observed link

## Observation: 
In general, link measurements are inevitably subject to error/inaccuracy. This error/inaccuracy will be **accumulated and propagated** to the relevant **inferred link flows**.
Different location schemes may have quite different accuracy accumulation and propagation results.
To enhance the reliability of link flow inference, it seems necessary to find a network sensor location scheme with **the minimized accumulated uncertainty**. 

## Problem:
For large-size relistic network, it is difficult to enumerate and evaluate all feasible schemes. 
(we can use evolutionary algorithm to solve the problem iteratively, but computationally expensive.) 

## Solution:
Each flow conservation equation is only able to independently determine a single unobserved link flow.
The fewer unobserved links involved in the flow conservation equation, the lower chance of accumulating measurement errors and uncertainty. 
So, the goal becomes to **minimize the largest(*model 1*) or the cumulative number(*model 2*) of unobserved links connected to each non-centroid node**. 

## Model 1: min-max problem
![image](https://user-images.githubusercontent.com/88390140/131718264-88485507-b24d-45a5-95b8-22eec50dfd84.png)
Reformulate:
![image](https://user-images.githubusercontent.com/88390140/131718361-bba33552-47aa-4295-843e-a115be9086fd.png)

 - N: the set of non-centroid nodes  
 - Ai: the set of new links connected to non-centriod node i 
 - xa = 1 if link a is selected; 0 otherwise 
 - Only one new link is selected from each non-centroid node ![image](https://user-images.githubusercontent.com/88390140/131719211-64a8f7ba-7454-4fdd-a639-b78512c9a893.png)
 - ![image](https://user-images.githubusercontent.com/88390140/131719347-a3420cc4-db07-4d61-afb8-425c5514d512.png) is the number of unobserved links connected to a non-centroid node i 


## Model 2: min-sum problem 
![image](https://user-images.githubusercontent.com/88390140/131718401-7f7faa01-3b69-4470-a224-cd78ad803c2d.png)

## Procedure
(1) Preparing the model input: **the set of new links**, node-link incidence matrix  
(2) Using algorithms (Mixed Integer Programming) to solve models in commercial software packages 

## Consideration of non-uniform measurement errors

## Extension: uncertainty reduction-oriented redundant sensor location problem 


