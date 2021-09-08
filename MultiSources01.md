#### Paper Link:
 - Wu, Xin et al. “[**Hierarchical travel demand estimation using multiple data sources: A forward and backward propagation algorithmic framework on a layered computational graph**](https://www.sciencedirect.com/science/article/pii/S0968090X18306685#f0015).” Transportation Research Part C-emerging Technologies 96 (2018): 321-346. 
 - [**A short tutorial of deep learning and computational graph frameworks in transportation modeling**](https://www.researchgate.net/publication/325126768)
 - 
 - https://ir.nctu.edu.tw/bitstream/11536/22104/1/000322432200002.pdf
 - https://www.sciencedirect.com/science/article/pii/S0968090X15000777?pes=vor
 - https://www.sciencedirect.com/science/article/pii/S0968090X15003101?pes=vor
 - 
 - https://www.sciencedirect.com/science/article/pii/S2352146515000800?pes=vor
 - http://t2r2.star.titech.ac.jp/rrws/file/CTT100742989/ATD100000413/
 - https://mdpi-res.com/applsci/applsci-11-02306/article_deploy/applsci-11-02306-v2.pdf
 - 
 - https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9213626

___________________________________________________________________________________________________________________________________________________________________________________
## [**Background: Backpropagation**](http://colah.github.io/posts/2015-08-Backprop/)

![image](https://user-images.githubusercontent.com/88390140/132399277-54e801ab-2fde-42b2-af88-e138a92337c0.png)
![image](https://user-images.githubusercontent.com/88390140/132399289-9089afe4-357b-46e8-80b2-61620d47c6fb.png)     
     
![image](https://user-images.githubusercontent.com/88390140/132399541-d47b3bf3-0ab4-412c-9e4f-ff522a32850e.png)
![image](https://user-images.githubusercontent.com/88390140/132399561-8e2ab6bd-73dd-4f0c-9ac0-1cd53180a146.png)

Forward-mode differentiation gave us the derivative of our output with respect to a single input, but reverse-mode differentiation gives us all of them.

## Benefit:   
When training neural networks, we think of the cost (a value describing how bad a neural network performs) as a function of the parameters (numbers describing how the network behaves). We want to calculate the derivatives of the cost with respect to all the parameters, for use in gradient descent. Now, there’s often millions, or even tens of millions of parameters in a neural network. So, reverse-mode differentiation, called backpropagation in the context of neural networks, gives us a massive speed up!    



