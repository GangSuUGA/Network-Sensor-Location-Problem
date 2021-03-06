## Resources Link:  
 - [**Traffic Forecasting Resource**](https://tfresource.org/) 
 - [**Figure Sources**](https://www.youtube.com/watch?v=y3T_DaDA3_c&list=PLLGIZCXnKbU6-9vy_rKZ6gW7E_ra42hfX)
_______________________________________________

## Why do we model? 
![image](https://user-images.githubusercontent.com/88390140/134061047-42bf4c32-71f5-4278-b3de-ba8556eac66c.png)

## How do we model? 
 - **Measure**: What get mearsures what get done. 
![image](https://user-images.githubusercontent.com/88390140/134061529-c93dfd86-96f2-4461-b1fb-79a65f2ad282.png)

## Viewpoints on Model: 
![image](https://user-images.githubusercontent.com/88390140/134062075-93b137d2-3af3-4024-b54e-0c2be4ce337d.png) 
![image](https://user-images.githubusercontent.com/88390140/134062290-4b36e894-ca84-4f96-a39a-6c2258cfa0d1.png)


## Distinction between the different types of traffic models:
- A macroscopic model uses fluid variables, such as flow and density, and does not model individual vehicles — these are aggregated into continuous variables. 
- A microscopic model describes vehicles (and often even drivers) individually. 
- A mesoscopic model is in between and combines the ideas from macroscopic and microscopic models. Typically it uses macroscopic speed–flow relations to depict the motions of individual vehicles.

## Four-Step Travel Demand Model

![image](https://user-images.githubusercontent.com/88390140/131938249-169a7b13-877a-4f33-9580-2bc3c4351fe4.png)     

Four-Step travel demand modeling is the traditional procedure utilized for transportation forecasts.

 - **Step 1: Trip Generation. – How many trips are generated/attracted?**      
The goal of trip generation (production) is to estimate the number of trips that are produced or originate in each Traffic Analysis Zone (TAZ). For each TAZ, it is estimated the extent to which it is an origin and destination. The output is usually the number of trips generated and attracted by a given TAZ. 

 - **Step 2: Trip Distribution. - O-D Matrix**    
Commonly a TAZ interaction model estimates movements (flows) between origins and destinations and which can consider constraints such as distance. The output is a O-D flow matrix between TAZ.  

 - **Step 3: Mode Choice. - What travel mode is used for each trip?**     
Mode Choice predicts the choices that individuals or groups make in selecting their transportation modes, which depends on the travel time/cost, accessibility to the public transit options and also social preferences.   

 - **Step 4: Traffic Assignment. – What is the route/link of each trip?**     
In the traffic assignment the OD-matrix for each mode is assigned onto the traffic network according to "User Equilibrium" (opposed to System Equilibrium), since each user chooses the route self-interest.  

________________________________
 - Torgil Abrahamsson (1998). [**Estimation of Origin-Destination Matrices Using Traffic Counts – A Literature Survey**](http://pure.iiasa.ac.at/id/eprint/5627/1/IR-98-021.pdf)
 - Bell, M. G. H. and Yasunori Iida. “[**Transportation Network Analysis**](https://www.wiley.com/en-us/exportProduct/pdf/9780471964933).” (1997). (Chapter 7) 

## Introduction: 
- Origin-Destination (OD) matrix provide information of traffic demands on the number of travelers that commute or the amount of freight shipped between differrent traffic analysis zones (TAZ). 
- OD matrix is difficult to obtain by direct measurements/household surveys, but by using traffic counts and other available information one may obtain a "reasonable" estimate. 
- Assigning an OD matrix to a transportation network means that the demand for traffic between every pair of zones is allocated to available routes connecting the zonal pairs. 
- From the assignment of the OD matrix one thus obtain the traffic volume on each link. 
- The "inverse" of the asssignment problem: find an OD matrix which reproduces the observed traffic counts. 
- Normally there is a large number of different OD matrices which reproduce the observed traffic counts. The related equation system is underspecified (or degenerate) and may have many possible solutions. 
- One may thus ask for the most "likely" or "best" OD matrix causing the observed traffic counts. 

## How to infer O-D from Traffic Count? (static)
- **Maximum Entropy** 
- **A Generalised Least Squares** 
- **Bi-Level Programming** 
- **Linear Path Flow Estimation** 
- **Log-Linear Path Flow Estimation** 
- **Time-Dependent Methods** 

![image](https://user-images.githubusercontent.com/88390140/135630187-37700680-c890-4961-b7b9-562c61e7a151.png)

