#### Paper Link:
 - Xu, Xiangdong et al. “[Robust network sensor location for complete link flow observability under uncertainty](https://www.sciencedirect.com/science/article/pii/S0191261516000436?via%3Dihub).” Transportation Research Part B-methodological 88 (2016): 1-20. 
 - [**Prerequisite**](https://github.com/GangSuUGA/The-Optimization-of-Sensor-Location/blob/main/Ob01_A_node-based_approach.md)
___________________________________________________________________________________________________________________________________________________________________________________
**Note:**  
- **Selecting any single new link just self-assumed the order/sequences of each non-centroid. Actually the order/sequence will influence the results.**        
- **This method still produce many solutions.**  

In this paper, the author provide a **robust** network sensor location model for complete link flow inference via a node-based approach while **considering the propagation of measurement errors**. 

## Sources of Error
#### (1)  Measurement Error 
 - (a) Loop data are often missing or invalid due to communication error or hardware breakdown.   
 - (b) Payne et al. (1976) identified various types of detector errors, such as stuck sensors, hanging on or hanging off, chattering, cross-talk, pulse breakup, intermittent malfunction, etc.   
 - (c) Even under normal conditions, loop detector measurements could be noisy, e.g., due to the confusion of multi-axle trucks.   
#### (2)  Also, errors can accumulate and propagate.   
#### (3)  The variablity or uncertainty of the observed link flows adds to the problem. In general, the measurements represent just a sample of the variable link flows.  

## Assumptions of this paper
(1) A new network/region, there is no existing sensor.   
(2) The measurements errors are not yet available 
(3) (From my perspective, I guess the author might want to assume the variability or uncertainty of each detector is same in order to make problem more ideal). 

## Example of a node-based approach
![image](https://user-images.githubusercontent.com/88390140/131739377-83d3519f-8bd6-423a-8f3d-16cd46d52ae8.png)
![image](https://user-images.githubusercontent.com/88390140/131739311-d5b60dbe-51f2-4f31-98b5-16e81f3d8cb6.png)  
![image](https://user-images.githubusercontent.com/88390140/131738532-1775df64-31ab-487a-ac18-1a8173bccc59.png)  
![image](https://user-images.githubusercontent.com/88390140/131738587-54fe9edc-2559-4b18-9ce3-6d6bc5f28d59.png)  

The flow variance on unobserved link a can be expressed as:      
![image](https://user-images.githubusercontent.com/88390140/131688630-5bd64c1b-63bd-49e8-8220-bec325ace1aa.png)
(a: unobersed link; b: observed link).       
![image](https://user-images.githubusercontent.com/88390140/131739911-33a4d7a4-79e2-4730-8efc-cc26c628b3b9.png)
, the relationship between the unobserved and observed link flows cannot be expressed generally and explicitly as **x** (a function of the sensor location scheme) can not be written directly to minimize the accumulated variance of inferred link flows propagated from measurement errors.   
**Instead, this paper proposes an indirect way to resolve this problem.**  

## Observation: 
In general, link measurements are inevitably subject to error/inaccuracy. This error/inaccuracy will be **accumulated and propagated** to the relevant **inferred link flows**.
Different location schemes may have quite different accuracy accumulation and propagation results.
To enhance the reliability of link flow inference, it seems necessary to find a network sensor location scheme with **the minimized accumulated uncertainty**. 

## Problem:
For large-size relistic network, it is difficult to enumerate and evaluate all feasible schemes. 
(we can use evolutionary algorithm to solve the problem iteratively, but computationally expensive.) 

## Solution:
 - **New Link Method**: Each flow conservation equation is only able to independently determine a single unobserved link flow.
 - The fewer unobserved links involved in the flow conservation equation, the lower chance of accumulating measurement errors and uncertainty. 
So, the goal becomes to **minimize the largest(*model 1*) or the cumulative number(*model 2*) of unobserved links connected to each non-centroid node**. 

## Model 1: min-max problem
![image](https://user-images.githubusercontent.com/88390140/131718264-88485507-b24d-45a5-95b8-22eec50dfd84.png)
Reformulate:
![image](https://user-images.githubusercontent.com/88390140/131718361-bba33552-47aa-4295-843e-a115be9086fd.png)

###  Notation
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
![image](https://user-images.githubusercontent.com/88390140/131761358-ae342ead-f3c6-4d79-adcd-e7de9167f4c4.png)     
This paper also add the variance bound, ![image](https://user-images.githubusercontent.com/88390140/131761639-11c03dfc-eaa7-4186-9373-7da2cac57f46.png)
as the minimum and maximum variance among all links respectively. 

## Extension: uncertainty reduction-oriented redundant sensor location problem 
**How many redundant sensors are needed for a certain level of uncertainty reduction?**


