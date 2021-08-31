Link flow inference is to infer the unobserved link flows based on the observed link flows. 
There are two main approaches to inferring link flows: node-based approach and link-based approach. 

# Node-based Approach
Let G = (V,E) denote a transportation network, where V denotes the set of nodes andEthe set of links. 
V is here further sub-divided into centroids and non-centroids. Nodes 1, 2,8 and 9 are centroids. The non-centroid nodes are all other nodes in the network. 
The non-centroid nodes can be determined by the known observability via centroids. 

![image](https://user-images.githubusercontent.com/88390140/131421589-186152da-d561-46b6-a595-d8f268416233.png)

The node-link incidence matrixA  of the network G is defined as the matrix with entriesgiven by: 
 
 ![image](https://user-images.githubusercontent.com/88390140/131421516-35edad06-0749-4a56-bda7-37b5226355b2.png)
 ![image](https://user-images.githubusercontent.com/88390140/131421836-809f20ae-de45-4f63-8ced-6b33e13f28a6.png)



