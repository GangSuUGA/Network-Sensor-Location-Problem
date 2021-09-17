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

## New Link Method (like previous one): 
Each link assigned to a set of new links related to a non-centroid node should be a link connected to that node and shouldn’t already be assigned to other sets of new links.      
![image](https://user-images.githubusercontent.com/88390140/133707671-67ccfe42-0fc0-422c-bbd1-4269d384671d.png)

## Assumption: 
 - The probability of failure of identical sensors is assumed to be the **same** regardless of their cost and their employed technology. 
 - This assumption can be beneficial when there are **not enough historical records** about the failure of different type of sensors. 
 - However, if this information is available, we can develop a more specific model considering **non-identical sensors having different probabilities of failure**.
 - Note that in both scenarios, we assume that the sensors are **installed independently** and there is **no correlation** between the failure of any pair of sensors.  

## Probability of missing the link flow inference of unobserved links:  
![image](https://user-images.githubusercontent.com/88390140/133790018-ff22f22d-3abe-4607-8928-24a3a3875bdd.png)
![image](https://user-images.githubusercontent.com/88390140/133789955-06b061bb-9be1-4ab5-9501-ee540967de47.png)

**The elements of the matrix −Tu −1 To can help us to identify the observed links that should be used for inferring the flow of an unobserved link.**

 - **Y1**: Minimize **the maximum probability** of missing the link flow inference of an unobserved link. 
 - **Y2**: Minimize **the expected number** of missing the link flow inference of an unobserved link. 
 
![image](https://user-images.githubusercontent.com/88390140/133790453-8abfb41d-ad02-44cb-9be1-e4f1f3b7d428.png)![image](https://user-images.githubusercontent.com/88390140/133795060-941f58d4-64fe-489a-ae00-f5be5e917f80.png)
  
The element aj′j′′ means row j′ and column j′′ of the matrix −Tu −1 To. 

**Why square the element?** 
 - Cancel the effect of negative signs. 
 - Helpful in identifying higher chance of missing link flow inference.     

## Recap: 
![image](https://user-images.githubusercontent.com/88390140/133792293-77a14cb2-2eb2-44ef-8df4-1ed953805f52.png)

## Effect of a sensor failure on the link flow inference of unobserved links: 
 - Minimize **the maximum expected number of unobserved links** for which their flow will be missed due to the failure of a sensor installed on an observed link.      
![image](https://user-images.githubusercontent.com/88390140/133802214-9e97b4fa-ffa6-47c7-a836-f307f4db731f.png)

## Mathematical Formulation: 
 - Objective functions: 
![image](https://user-images.githubusercontent.com/88390140/133805769-0adcbd88-ed61-499f-8ee1-6aa0de47303b.png)

 - Constraints regarding identical roads:      
![image](https://user-images.githubusercontent.com/88390140/133805816-5ae170fa-6600-4fe6-985b-e6f65ebb8acc.png)    
![image](https://user-images.githubusercontent.com/88390140/133805831-caf9b718-8811-4843-b8fd-e939b58d5da1.png)   hij: New Link Matrix

 - Constrains considering major roads:      
![image](https://user-images.githubusercontent.com/88390140/133806020-abf3b10e-ac97-46c4-8956-a748f0623849.png)



