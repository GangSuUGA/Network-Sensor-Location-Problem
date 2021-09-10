#### Paper Link:
 - Wu, Xin et al. “[**Hierarchical travel demand estimation using multiple data sources: A forward and backward propagation algorithmic framework on a layered computational graph**](https://www.sciencedirect.com/science/article/pii/S0968090X18306685#f0015).” Transportation Research Part C-emerging Technologies 96 (2018): 321-346. 
 - [**A short tutorial of deep learning and computational graph frameworks in transportation modeling**](https://www.researchgate.net/publication/325126768)
 - [**Prerequisite (backpropagation)**](https://github.com/GangSuUGA/The-Optimization-of-Sensor-Location/blob/main/MulSou01Background.md)
 - https://www.bilibili.com/video/BV14g411L7rL?from=search&seid=3384406637636649164&spm_id_from=333.337.0.0
___________________________________________________________________________________________________________________________________________________________________________________

The overarching rationale of transportation system intelligence is that developments in **sensing, cyber-physical infrastructures, and crowdsouring big data technologies** can be integrated to effecitive use for improving the performance of transportation systems.    

**Early "traffic demand flow estimation" model focus on estimating origin/destination (OD) matrices from traffic counts.**     

**This paper first proposes a multi-layered Hierarchical Flow Network (HFN) to structurally model different levels of travel demand variables using multiple data sourses. 

The demand variables including trip generatin, origin/destination matrices, path/link flow, and individual behavior parameters. ([**traffic four step**](https://github.com/GangSuUGA/The-Optimization-of-Sensor-Location/blob/main/Background_Traffic_ODmatrix.md))       

## Multiple data sources:    

![image](https://user-images.githubusercontent.com/88390140/132562210-73e559a4-43f5-46d2-bdfb-be3381160085.png)   
![image](https://user-images.githubusercontent.com/88390140/132582273-67b11474-35d7-4fd1-b822-f19518333896.png)


**Household travel surveys** can provide trip production and abstraction from zones and sometimes OD trip tables between the zones.     

A number of studies are devoted to finding how to incorporate **Mobile phone sample data** into activity-based models to estimate trip chain behavior.    

**GPS/Floating car Data** can be used to estimate the observed travel time of links and establish urban traffic indexes.     

Large volumes of observed link counts can be collected from **sensors** including inductive loops,radars,cameras,etc.    

## The four-layered HFN representation: 
![image](https://user-images.githubusercontent.com/88390140/132875818-b44462d1-91b9-4043-aa86-ce5fbf8e26e1.png)
![image](https://user-images.githubusercontent.com/88390140/132875883-f0c777a1-ddba-47d2-bfc9-cb4863f44695.png)



_________________________________________________________________________________________________________________
Wei Ma PolyU
![image](https://user-images.githubusercontent.com/88390140/132875524-fb871485-8b3f-46e1-bac2-9464dd587b6c.png)
![image](https://user-images.githubusercontent.com/88390140/132875253-effd55a3-f80d-477f-bf9e-e34df9d5ded3.png)
![image](https://user-images.githubusercontent.com/88390140/132875374-4e21d73e-db68-4b73-82c3-1f4b384f4d2f.png)

