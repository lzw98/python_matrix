### 从对角化到特征向量
针对表达式$P^{-1}AP=\Lambda$,我们可以得到$A P=P \Lambda$，因此我们有
$$A\left[\begin{array}{lllllllll}p_{1} & p_{2} & p_{3} & \ldots & p_{n}\end{array}\right]=\left[\begin{array}{ccccc}p_{1} & p_{2} & p_{3} & \ldots & p_{n}\end{array}\right]\left[\begin{array}{cccc}\lambda_{1} & & & \\ & \lambda_{2} & & \\ & & & \lambda_{3} & \\ & & & & \cdots \\ & & & & & \lambda_{n}\end{array}\right]$$

最终得到了:
$$\left[\begin{array}{llllllll}
A p_{1} & A p_{2} & A p_{3} & \ldots & A p_{n}
\end{array}\right]=\left[\begin{array}{llllll}
\lambda_{1} p_{1} & \lambda_{2} p_{2} & \lambda_{3} p_{3} & \ldots & \lambda_{n} p_{n}
\end{array}\right]$$

这样就知道了求对角化的过程，其实就是在求特征向量与特征值的过程。

#### 几何意义
对于一个指定的向量v，如果我使用默认的基底$(e_1,e_2,...,e_n)$对其进行表示为：$x_1e_1+..+x_ne_n$。使用方阵A对其进行线性变换，紧接我们采用A的一组特征向量来作为新的基底。则该向量表示为$y_1p_1+y_2p_2+...+y_np_n$,在新的基底下，其坐标为$[y_1,y_2,...,y_n]^T$,在此基础上对该向量进行线性变换A，$A\left(y_{1} p_{1}+y_{2} p_{2}+y_{3} p_{3}+\ldots+y_{n} p_{n}\right)$

$$A y_{1} p_{1}+A y_{2} p_{2}+A y_{3} p_{3}+\ldots+A y_{n} p_{n}=\lambda_{1} y_{1} p_{1}+\lambda_{2} y_{2} p_{2}+\lambda_{3} y_{3} p_{3}+\ldots+\lambda_{n} y_{n} p_{n}$$

这个等式的推导结果可以是非常漂亮的，利用新的基底所表示的向量，经过矩阵的线性转换之后，其基底在保持不变的前提下，向量坐标由$[y_1,y_2,...,y_n]^T$变成$[\lambda_1y_1,\lambda_2y_2,...,\lambda_ny_n]^T$

***概括来说：对于一个特定向量施加矩阵A所描述的线性变换，如果使用矩阵A的特征向量($p_1,p_2,...,p_n$)作为空间的基底来对该向量进行坐标表示，则该空间变换即可简化为各个维度的坐标值在其基向量的方向上对就伸缩常数倍***

#### 基本的几何性质 
- case1:如果存在矩阵特征值为0的情况，那么有$A p=O p=0$，这就意味着，该矩阵表示的是空间的压缩，说明这是一个不可逆矩阵，即奇异阵
- case2:对角阵，则其对角元素即为其特征值。
- case3:相似矩阵有相同的特征值
- 不同特征值所对应的特征向量一定没有线性相关关系，相同特征值所对应的特征向量也不一定线性相关。