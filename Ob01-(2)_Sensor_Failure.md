## Paper Link:
 - Salari, M. et al. “[**Optimization of traffic sensor location for complete link flow observability in traffic network considering sensor failure**](https://reader.elsevier.com/reader/sd/pii/S0191261518307288?token=D7668AECA1C83B05C4E6AD894DE9A05E657BC1E9379837606CC701F697B1A2CC659BE43E7CEF31F9091FFAEA6AFD8893&originRegion=us-east-1&originCreation=20210912024131).” Transportation Research Part B-methodological 121 (2019): 216-251.
 - 


_____________________________________________

## Motivating Example and Observation: 
 - The flow of an unobserved link cannot be inferred if at least one of the sensors installed on the observed links in that equation breaks down.
 - Considering the failure probability of sensors located on the observed links, we can calculate **the probability of missing/not inferring the link flow of unobserved links**. 
![image](https://user-images.githubusercontent.com/88390140/133706814-e95ec274-b9a0-4f12-87cf-1d1c1ad1dbb9.png)

 - In addition, we are also interested in exploring the effect of a sensor’s failure on the link flow inference of unobserved links. 
![image](https://user-images.githubusercontent.com/88390140/133707198-93b20e28-0fd6-4dcc-b0be-0b4b6ebd2325.png)

 - According to this column, **the lower the number of appearances of an observed link in different equations** required for the link flow inference of unobserved links, **the lower the expected number of unobserved links for which flow cannot be inferred** due to the failure of the sensor installed on that observed link. 

## New Link Method: 
Each link assigned to a set of new links related to a non-centroid node should be a link connected to that node and shouldn’t already be assigned to other sets of new links.      
![image](https://user-images.githubusercontent.com/88390140/133707671-67ccfe42-0fc0-422c-bbd1-4269d384671d.png)
