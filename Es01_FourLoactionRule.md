#### Paper Link:
 - Yang, Hai et al. “[**An analysis of the reliability of an origin-destination trip matrix estimated from traffic counts**](https://www.sciencedirect.com/science/article/pii/019126159190028H?pes=vor).” Transportation Research Part B-methodological 25 (1991): 351-363.       
 - Yang, Hai and J. Zhou. “[**Optimal traffic counting locations for origin–destination matrix estimation**](https://www.sciencedirect.com/science/article/pii/S0191261597000167?via%3Dihub).” Transportation Research Part B-methodological 32 (1998): 109-126.
 - [**Background: OD Trip Table Estimation**](https://github.com/GangSuUGA/The-Optimization-of-Sensor-Location/blob/main/Background02:%20Trip%20Table%20Estimation.md) 
__________________________________________________

## Motivation 
- - **Definition of OD Estimation**: The estimation of OD trip matrices aims at choosing a matrix with a high degree of accuracy or reliability among many possible ones satisfying the traffic count constraints. 
- Typically, the **Entropy Maximizing, Information Minimizing, and Least Squares Estimators** have been proposed and applied. 
- **Problem**: Since the **"true" OD trip matrix** is unknown, it is impossible to evaluate exactly the estimation accuracy. 
- Yang, Hai et al. (1991) proposed "Maximum Possible Relative Error (MPRE)" to investigate the reliability of an estimated OD trip matrix. 

## Maximum Possible Relative Error (MPRE) 
- **Method**: Calculating an upper bound or maximum possible relative error. 
![image](https://user-images.githubusercontent.com/88390140/135565833-6d4ee76d-ad0e-4001-b57c-199f28cdd59a.png)

- **Theoretical Formulation**:         
![image](https://user-images.githubusercontent.com/88390140/135566497-158ac894-3e45-4069-b39d-b4d92fc8555e.png)
![image](https://user-images.githubusercontent.com/88390140/135566539-96143314-cdd7-4e6f-85d0-465eb44b12c8.png)
![image](https://user-images.githubusercontent.com/88390140/135566569-c4b638ae-783e-40f6-b433-c885fff25593.png)
![image](https://user-images.githubusercontent.com/88390140/135566577-323b0e99-3477-4e4f-bb09-2f409272261c.png)
![image](https://user-images.githubusercontent.com/88390140/135566598-585203fa-ec01-4cfd-a089-b9d12cc30416.png)
![image](https://user-images.githubusercontent.com/88390140/135566826-093b076a-a4b0-4af8-9f35-5e5c6f73682c.png)

## Reform: 
![image](https://user-images.githubusercontent.com/88390140/135566907-f967754a-4f72-48ba-8ab1-ce1af56f7a82.png)
![image](https://user-images.githubusercontent.com/88390140/135566940-3c3bfb2e-e5fe-4c85-a95b-4c673182a083.png)
![image](https://user-images.githubusercontent.com/88390140/135566968-b8ee5bb1-4286-40ca-a4bd-2f04d6a06cd2.png)           
The Maximum Possible Average Relative Error can be extended to incorporate other prior information by **considering the relative magnitudes of OD volumes**.        
![image](https://user-images.githubusercontent.com/88390140/135566997-dfa52284-9df7-4a7c-8815-c671e2b37b48.png)

## Observation: 
![image](https://user-images.githubusercontent.com/88390140/135631940-b6507272-f01a-4b2b-a605-85181581a582.png)       
In this situation, ![image](https://user-images.githubusercontent.com/88390140/135632115-24ef37d0-fa62-4978-af04-9752db8af352.png) is unbounded, which also means the trips between the jth OD pair do not pass over any of the observed links. In other words, if there are no traffic counters to observe this OD pair, the corresponding ![image](https://user-images.githubusercontent.com/88390140/135632115-24ef37d0-fa62-4978-af04-9752db8af352.png) will become infinite.         
On the contray, ![image](https://user-images.githubusercontent.com/88390140/135632597-5044669f-072f-4ece-b5bd-d7ab60406d55.png)      
In other words, if there is at least one traffic counter to observe this OD pair, the corresponding ![image](https://user-images.githubusercontent.com/88390140/135632115-24ef37d0-fa62-4978-af04-9752db8af352.png) will become infinite.

## Rule 1 (O-D covering rule):     
The traffic counting points on a road network should be located so that **a certain portion of trips between any O-D pair will be observed**.       

![image](https://user-images.githubusercontent.com/88390140/135634859-955d4cff-698c-4af0-b0da-24d522e34133.png)

## Rule 2 (maximal flow fraction rule):     
For a particular O-D pair, the traffic counting points on a road network should be located at the links so that **the flow fraction between this O-D pair out of flows on these links is as large as possible**. 

## Example      
![image](https://ars.els-cdn.com/content/image/1-s2.0-S0191261597000167-gr1.gif)        
![image](https://user-images.githubusercontent.com/88390140/135644290-26b1f134-f2bb-433b-8a0b-716224ed4a60.png)    
![image](https://user-images.githubusercontent.com/88390140/135644613-5be1512a-6bb7-4b82-b8de-d1e1c00364f5.png)

- Observation: For example, the set of (d;e) is less desirable than (a;b) and (c;d), because the latter can intercept all flows through the network.        
## Rule 3 (maximal flow-intercepting rule):      
Under a certain number of links to be observed, the chosen links should **intercept as many flows as possible**. 

## Observation: 
Because the flow conservation equation (like Va + Vb = Vc + Vd), links a, b, c and d should not be chosen simultaneously. In this situation, ![image](https://user-images.githubusercontent.com/88390140/135645677-9fef6a54-ab37-45df-80b0-417ebdf84b45.png) will become linearly dependent.     
      
## Rule 4 (link independence rule):     
The traffic counting points should be located on the network so that **the resultant traffic counts on all chosen links are not linearly dependent**. 
