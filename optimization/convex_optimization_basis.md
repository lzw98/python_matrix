## chapter1 优化导入
首先优化可以分为以下几类
- 线性与非线性
- 凸与非凸
- 针对可行域而言分为：连续和离散
- 单目标和多目标

本文的主要内容是：
- 凸集，凸函数，凸优化
- 凸优化理论
- 若干算法

## chapter2 凸集(convex sets)

#### 仿射集(Affine sets)
> 定义直线：若$x_1\neq x_2\in R^n,\theta \in R \qquad y = \theta x_1+(1-\theta)x_2$
- 定义线段：若$x_1\neq x_2\in R^n,\theta \in R \qquad y = \theta x_1+(1-\theta)x_2，\theta \in [0,1]$

- 定义仿射集：若$\forall x_1,x_2 \in C$,则连接$x_1,x_2$的直线也在集合内的集合C为仿射集。
- 数学表达为：$设x_1,...,x_k \in C,\theta_1,\theta_2,...,\theta_k \in R,\theta_1+\theta_2+...+\theta_k=1,则有 \theta_1x_1+\theta_2x_2+...+\theta_kx_k\in C$

例：线性方程组的解集是仿射集
$$C = {x|Ax=b},A\in R^{m\times n},b\in R^{m},x \in R^n$$
$$\forall x_1,x_2 \in C 则有Ax_1 = b,Ax_2 = b,易知\theta_1x_1+(1-\theta)x_2\in C$$

#### 凸集(convex set)
- 定义凸集: $\forall x_1,x_2 \in C ,\forall \theta \in [0,1],\theta x_1+(1-\theta)x_2 \in C$
- 定义凸组合：$x_1,..,x_k的凸组合,\theta_1+...+\theta_k=1,\theta_1...\theta_k \in R,则称[\theta_1x_1+...+\theta_kx_k]为凸组合$
- $$C为凸集\iff 任意元素的凸组合\in C$$

- 定义凸包：$x_1,..,x_k的凸包,\theta_1+...+\theta_k=1,\theta_1...\theta_k \in[0,1] ,则称[\theta_1x_1+...+\theta_kx_k]为凸包，记为conv c$