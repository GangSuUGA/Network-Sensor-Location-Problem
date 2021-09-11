#### Paper Link:
 - Wu, Xin et al. “[**Hierarchical travel demand estimation using multiple data sources: A forward and backward propagation algorithmic framework on a layered computational graph**](https://www.sciencedirect.com/science/article/pii/S0968090X18306685#f0015).” Transportation Research Part C-emerging Technologies 96 (2018): 321-346. 
 - [**A short tutorial of deep learning and computational graph frameworks in transportation modeling**](https://www.researchgate.net/publication/325126768)
 - 
 - Lu, C. et al. “[**Dynamic origin-destination demand flow estimation under congested traffic conditions**](https://ir.nctu.edu.tw/bitstream/11536/22104/1/000322432200002.pdf).” Transportation Research Part C-emerging Technologies 34 (2012): 16-37.
 - Shi, Q. and M. Abdel-Aty. “[**Big Data applications in real-time traffic operation and safety monitoring and improvement on urban expressways**](https://www.sciencedirect.com/science/article/pii/S0968090X15000777?pes=vor).” Transportation Research Part C-emerging Technologies 58 (2015): 380-394.
 - Antoniou, C. et al. “[**Towards a generic benchmarking platform for origin–destination flows estimation/updating algorithms: Design, demonstration and validation**](https://www.sciencedirect.com/science/article/pii/S0968090X15003101?pes=vor).” Transportation Research Part C-emerging Technologies 66 (2016): 79-98.
 - 
 - Wu, Cathy et al. “[**Cellpath: Fusion of Cellular and Traffic Sensor Data for Route Flow Estimation via Convex Optimization**](https://www.sciencedirect.com/science/article/pii/S2352146515000800?pes=vor).” Transportation research procedia 7 (2015): 212-232.
 - Seo, T. et al. “[**Traffic state estimation on highway: A comprehensive survey**](http://t2r2.star.titech.ac.jp/rrws/file/CTT100742989/ATD100000413/).” Annu. Rev. Control. 43 (2017): 128-151.
 - Cvetek, Dominik et al. “[**A Survey of Methods and Technologies for Congestion Estimation Based on Multisource Data Fusion**](https://mdpi-res.com/applsci/applsci-11-02306/article_deploy/applsci-11-02306-v2.pdf).” Applied Sciences 11 (2021): 2306.
 - 
 - Chenyang, Yang et al. “[**A Modified Stochastic User Equilibrium Based Back-Propagation Method of Transportation Network State Estimation**](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9213626).” 2020 IEEE International Conference on Advances in Electrical Engineering and Computer Applications( AEECA) (2020): 442-447.

___________________________________________________________________________________________________________________________________________________________________________________
# **Now Pytorch/Tensorflow have autograd function to solve backpropagation automatically.**

## [**Background: Backpropagation**](http://colah.github.io/posts/2015-08-Backprop/)

![image](https://user-images.githubusercontent.com/88390140/132399277-54e801ab-2fde-42b2-af88-e138a92337c0.png)
![image](https://user-images.githubusercontent.com/88390140/132399289-9089afe4-357b-46e8-80b2-61620d47c6fb.png)     
     
![image](https://user-images.githubusercontent.com/88390140/132399541-d47b3bf3-0ab4-412c-9e4f-ff522a32850e.png)
![image](https://user-images.githubusercontent.com/88390140/132399561-8e2ab6bd-73dd-4f0c-9ac0-1cd53180a146.png)

Forward-mode differentiation gave us the derivative of our output with respect to a single input, but reverse-mode differentiation gives us all of them.

## Benefit:   
When training neural networks, we think of the cost (a value describing how bad a neural network performs) as a function of the parameters (numbers describing how the network behaves). We want to calculate the derivatives of the cost with respect to all the parameters, for use in gradient descent. Now, there’s often millions, or even tens of millions of parameters in a neural network. So, reverse-mode differentiation, called backpropagation in the context of neural networks, gives us a massive speed up!    



