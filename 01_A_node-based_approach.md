#### Paper Link:
#### Ng, Manwo. “Synergistic sensor location for link flow inference without path enumeration: A node-based approach.” Transportation Research Part B-methodological 46 (2012): 781-788. https://www.sciencedirect.com/science/article/pii/S0191261512000161
#### Xu, Xiangdong et al. “Robust network sensor location for complete link flow observability under uncertainty.” Transportation Research Part B-methodological 88 (2016): 1-20. http://www.math.wm.edu/~rrkinc/hmk_current/NLT/SensorLoc2016.pdf
#### Castillo, E. et al. “Matrix Tools for General Observability Analysis in Traffic Networks.” IEEE Transactions on Intelligent Transportation Systems 11 (2010): 799-813. https://ieeexplore.ieee.org/document/5482130
___________________________________________________________________________________________________________________________________________________________________________________


Link flow inference is to infer the unobserved link flows based on the observed link flows. 
There are two main approaches to inferring link flows: node-based approach and link-based approach. 
Specifically, the node-based approach uses the non-centroid node-link flow conservation equations while the link-based approach uses the link-path flow conservation equations.
To avoid path enumeration (which is impractical for large-scale networks), researchers adopt the node-based approach. (X. Xu et al., 2016)

# Node-based Approach
Let G = (V*,E) denote a transportation network, where V* denotes the set of nodes and E the set of links. 
V* is here further sub-divided into centroids and non-centroids. Centroids are the nodes where traffic originates/is destined to. (Nodes 1, 2,8 and 9 are centroids.)
The non-centroid nodes are all other nodes in the network (denote as V). Assume |V|=n and |E|=m. 
##### v = [v13, v14, v23, v24, v35, v36, v45, v47, v56, v57, v68, v69, v78, v79]T. (The v can be seen as E.) 
All unobserved link flows can be inferred from the observed flows. 

![image](https://user-images.githubusercontent.com/88390140/131421589-186152da-d561-46b6-a595-d8f268416233.png)

The node-link incidence matrix A* of the network G is defined as the matrix with entriesgiven by: 
 
 ![image](https://user-images.githubusercontent.com/88390140/131421516-35edad06-0749-4a56-bda7-37b5226355b2.png)
 
 The modified node-link incidence matrix A is obtained by deleting the rows in A* associated with the centroids. 
 ![image](https://user-images.githubusercontent.com/88390140/131421836-809f20ae-de45-4f63-8ced-6b33e13f28a6.png)

### Flow Conservation (Input = Output):     A v = 0   

![image](https://user-images.githubusercontent.com/88390140/131422958-c9c03726-35a8-432a-b15c-3d397fbf3c5b.png)
![image](https://user-images.githubusercontent.com/88390140/131422965-f927162c-5430-4741-8619-91889728077d.png)

The critial issue is to ensure the existence of (and find) the invertible matrix B. 
(B: an invertible matrix; N: a not necessarily invertible matrix.)

## Proposition 1
It is always possible to partition A into two matrices B and N, where B is an n-by-n invertible matrix. (Proof in reference) 

### One Solution 
![image](https://user-images.githubusercontent.com/88390140/131424603-d23982f1-d893-4a9e-b220-8882fde1d2a7.png)
The Vehicular flows on the links (13, 14, 35, 36, 47) can be infered from the sensor measurements on the remainder of the links via 
![image](https://user-images.githubusercontent.com/88390140/131422965-f927162c-5430-4741-8619-91889728077d.png)
The matrix B is not unique, another solution is (36, 47, 57, 69, 79). 

## Proposition 2
(Minimum number of sensors for full observability). Given a transporation network G = (V*, E). In order to observe all link flows in G, at a minimum, sensors need to be installed on (m-n)/m * 100% of the links. 
(Proof: The number of nodes means the number of independent formulations of flow conservation and hence means the number of unknown we can solve. So at most n link flows can be infered from sensor measurements. Hence, at least m-n link flows need to be measured.) 

## Proposition 3
(Integrality of inferred link flows). If vN is integral, vB will be integral as well. 
(Proof: From the perspective of flow conservation, each input or output components is caculated from adding or substracting.) 

## Questions/Considerations   
However, the node-based approach assumed that currently there are no sensors in the road network. In reality, there might often already be sensors present on certain links. Two relevant questions then arise.  
#### First, given that sensors are already present on the links in the subset R in E, in order to achieve full link observability, which additional subset of links should be equipped with sensors? 
#### Second, given that sensors are present on the links in the subset R in E, what link flows can be inferred from them? 

Castillo et al. (2010) addressed these questions in terms of the path-link incidence matrix (a link-based approach). 
