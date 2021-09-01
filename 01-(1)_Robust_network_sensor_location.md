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




