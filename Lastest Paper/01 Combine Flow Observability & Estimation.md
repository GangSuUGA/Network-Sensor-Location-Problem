#### Paper Link:
 - N. Zhu et al. (2021) [**A network sensor location problem for link flow observability and estimation**](https://www.sciencedirect.com/science/article/abs/pii/S0377221721008870)
__________________________________________________

## FLow Observability 
![image](https://user-images.githubusercontent.com/88390140/151836820-eb9855ac-ad9f-4d12-ace8-bb93716ada38.png)![image](https://user-images.githubusercontent.com/88390140/151826236-2eaf206f-b06b-4445-a08f-e8755f1ad3ae.png)
            
![image](https://user-images.githubusercontent.com/88390140/151827085-b8386ca2-b813-4bba-945d-9ca08b884697.png)![image](https://user-images.githubusercontent.com/88390140/151827130-a931b865-dc9c-4875-94dd-24eb7a316272.png)![image](https://user-images.githubusercontent.com/88390140/151827172-5fcf3234-eb77-497a-b53f-69f3334bc33b.png)![image](https://user-images.githubusercontent.com/88390140/151838589-4b71fe24-9827-4d8d-97be-dc0339132602.png)





- State Constraint: under the condition of full observability, a link should be in either the observed state or the inferred state. 
![image](https://user-images.githubusercontent.com/88390140/151835701-239c8ac0-6d67-46b0-87af-968bfd7b21b7.png)          
- Inference Constraint: ![image](https://user-images.githubusercontent.com/88390140/151835744-74cabf16-b77d-418f-a363-b2e445fb9788.png) ![image](https://user-images.githubusercontent.com/88390140/151829241-8b6c92a0-d88b-4460-8e4e-04321498b33f.png)

- Degree Constraint:             
The total number of observed and inferred links connected to each node is equal to the degree of that node. (**More details in paper**) ![image](https://user-images.githubusercontent.com/88390140/151835534-2273f462-9bf3-4484-8e9c-2b94f0e5eeb2.png)
![image](https://user-images.githubusercontent.com/88390140/151835587-8e2068c6-f5c5-4424-b0df-f07f50161533.png)

- Single-link Constraint: concerns a speical case in which node i is connected to only one link (see node 1). ![image](https://user-images.githubusercontent.com/88390140/151835942-da13a263-bd74-4843-9c63-df0f4ff11cea.png)


#### Now that constraint (5) and (6) can be linearized by two additional binary variables as described below: 
![image](https://user-images.githubusercontent.com/88390140/151836166-898dec1b-8d24-4d24-b950-1c62939a9d25.png)

### Conclusion: 
- The objective function of our sensor location model is to minimize the installation cost of sensors for full link flow observability and inference, where C_ij is the unit cost for locating and maintaining sensors on link (i,j). Basic Model (BM): 
![image](https://user-images.githubusercontent.com/88390140/151836503-f11200ef-3e8e-4d7a-8a2c-9f44eb52faf3.png)   
- We observe that in the absence of any cycles in the network, the priority variables Z_ij, which associated with constraints (3) and (4) and the linear constraints (7)-(14), are useless and can be removed to simplify our model. 
- When the total number of sensors is less than the optimal objective function value of BM, this indicates that full observability connot be achieved. 
- Hence, the paper extend model to bridge flow estimation via linear regression. 




































