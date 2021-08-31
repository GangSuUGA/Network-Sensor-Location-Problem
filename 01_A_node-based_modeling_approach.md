#### Resources Link:
#### Ng, Manwo. “Synergistic sensor location for link flow inference without path enumeration: A node-based approach.” Transportation Research Part B-methodological 46 (2012): 781-788.
https://www.sciencedirect.com/science/article/pii/S0191261512000161
==========================================================================

Link flow inference is to infer the unobserved link flows based on the observed link flows. 
There are two main approaches to inferring link flows: node-based approach and link-based approach. 

# Node-based Approach
Let G = (V,E) denote a transportation network, where V denotes the set of nodes andEthe set of links. 
V is here further sub-divided into centroids and non-centroids. Nodes 1, 2,8 and 9 are centroids. The non-centroid nodes are all other nodes in the network. 
The non-centroid nodes can be determined by the known observability via centroids. 
##### v = [v13, v14, v23, v24, v35, v36, v45, v47, v56, v57, v68, v69, v78, v79]T. (The v can be seen as E.) 

![image](https://user-images.githubusercontent.com/88390140/131421589-186152da-d561-46b6-a595-d8f268416233.png)

The node-link incidence matrixA  of the network G is defined as the matrix with entriesgiven by: 
 
 ![image](https://user-images.githubusercontent.com/88390140/131421516-35edad06-0749-4a56-bda7-37b5226355b2.png)
 ![image](https://user-images.githubusercontent.com/88390140/131421836-809f20ae-de45-4f63-8ced-6b33e13f28a6.png)

### Flow Conservation (Input = Output):     A v = 0   

![image](https://user-images.githubusercontent.com/88390140/131422958-c9c03726-35a8-432a-b15c-3d397fbf3c5b.png)
![image](https://user-images.githubusercontent.com/88390140/131422965-f927162c-5430-4741-8619-91889728077d.png)

The critial issue is to ensure the existence of (and find) the invertible matrix B. 
It is always possible to partition A into two matrices B and N, where B is an n-by-n invertible matrix. 
