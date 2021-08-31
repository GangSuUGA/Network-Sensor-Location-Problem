Link flow inference is to infer the unobserved link flows based on the observed link flows.
There are two main approaches to inferring link flows:  node-based approach and link-based approach.
Specifically, the node-based approach uses the non-centroid node-link flow conservation equations while the link-based approach uses the link-path flow conservation equations.
To avoid path enumeration (which is impractical for large-scale networks), researchers adopt the node-based approach. (X. Xu et al./Transportation Research Part B 88 (2016) 1-20) 

However, the node-based approach assumed that currently there are no sensors in the road network. In reality, there might often already be sensors present on certain links. Two relevant questions then arise.  
#### First, given that sensors are already present on the links in the subset R in E, in order to achieve full link observability, which additional subset of links should be equipped with sensors? 
#### Second, given that sensors are present on the links in the subset R in E, what link flows can be inferred from them? 

Castillo et al. (2010) 
