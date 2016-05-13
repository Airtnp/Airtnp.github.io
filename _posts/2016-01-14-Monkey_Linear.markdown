---
layout:     post
title:      "猴子也看不懂的线性代数入门"
subtitle:   "自娱自乐"
date:       2016-01-14 00:24:00
author:     "Airtnp"
header-img: "img/post-notes.jpg"
tags:
    - Notes
    - Math
    - Linear Algebra
---


## 1. 矩阵

###线性方程组
* 克拉默
* 快速计算的分解
|分解|形式|注|
|---|---|---|
|LU分解|$A=LU(P_\textrm{permutation})$|（可逆）上三角x下三角（阶梯式）|
|QR分解|$A=QR$|正交x上三角（格拉姆施密特正交化）|
|SVD分解|$A=U\Sigma V^{T}$|最小二乘解|
|LDU分解|$A=LDU$||
|LDLT分解|$A=LDL^T$||
|FFT/DFT|傅里叶形式+优化算法|三角正交基（卷积意义） $\int \cos{nx}\sin{mx} dx = 0$|

####SVD分解
* $A:M(m\times n)$将行空间($R_n$)映射到列空间+零空间($R_m + $)
* $U,V$单位化（格拉姆施密特单位化），$U^{T} = U^{-1}$
* $AV=  U \Sigma \Rightarrow A=U\Sigma V^{T}$
> 如果A存在零空间，那么行空间是$r$维，零空间是$n-r$维，我们同样可以取一组正交基。如果基零空间的向量为$v_{r+1},...,v_n$，那么$Av_{r+1}$将得到零向量，得到对角阵$Σ$对角线下方有一些$0$。需要把整个$R_n$空间的标准正交基完善成整个$R_m$空间的标准正交基，在对角阵$Σ$中用$0$来完善

* $AA^{T} = U\Sigma^2U^{T} \qquad A^TA = V \Sigma^2 V^T$
* ![SVD2.jpg-36.6kB][1]
* ![SVD.jpg-10.7kB][2]
> 从图中可以看到Σ虽然为$M \times N$矩阵，但从第$N+1$行到$M$行全为零，因此可以表示成$N \times N$矩阵，又由于右式为矩阵相乘，因此U可以表示为$M \times N$矩阵，$V^T$可以表示为$N \times N$矩阵


###线性算子
####例：微分方程
* 微分算子是一个线性算子
* 化为解零空间问题 $$aD^2y+bDy+cy = 0 \Rightarrow (aD^2+bD+c)y = 0 \Rightarrow L y= 0$$
* 化为求特征值问题
* + 指数函数是微分算子（微分是切空间变换）的特征向量（函数）
* + 矩阵指数函数，化为$(S^{-1}\Lambda S)^n = S^{-1}\Lambda^n S$或若当型
* + 常数变易法-线性方程(+Bernoulli/Riccati)
* + - 齐次解 $\sum cx(t)$ 非齐次 $\sum c(t)x(t)$ 
* + 朗斯基行列式-基解矩阵-一般化常数变易法 
$$W(f_1, \ldots, f_n) =
\begin{vmatrix} 
f_1 & f_2 & \cdots & f_n \\
f_1' & f_2' & \cdots & f_n' \\
\vdots & \vdots & \ddots & \vdots \\
f_1^{(n-1)} & f_2^{(n-1)} & \cdots & f_n^{(n-1)}
\end{vmatrix}$$
![Variation1.png-56.6kB][3]
![Variation2.png-86.6kB][4]
* + $$\varphi(t) = \sum_{k = 1}^{n} x_k(t) \int_{t_0}^{t} \frac{W_k(X(s))}{W(X(s))}f(s)ds$$
* + 微分方程解$$y = \sum c_ix_i(t) + \varphi(t)$$

![Differential Equation.png-41.4kB][5]
![Differential Equation_2.png-13.9kB][6]


###基/向量
![Space.png-67.4kB][7]
####列向量空间 $M$(M x N)
* $C(A)$ 列空间（$Ax = V$的V(span)空间）， $R_m$，向量有$m$个分量, $Dim(C(A)) = r$（秩，最大线性无关向量数）
* $N(A)$ 零(核)空间（$Ax = 0$的解空间）， $R_n$,$Dim(N(A)) = n-r$
* $C(A^T)$ 行空间， $R_n$,$Dim(C(A^T)) =  r$，
* + 矩阵转置后，列空间的维度不变
* $N(A^T)$ 转置的零空间，在 $R_m$,$Dim(N(A^T)) = m-r$

####增广矩阵
* 系数矩阵与增广矩阵同秩=> 解
* 说明新增列向量含在列空间中，为线性相关，为系数矩阵列向量线性组合
* 和高斯-约尔当消元法等价

###多项式/二次型
* 矩阵多项式
* 见《矩阵论》



###☆**有限维线性空间的线性变换**
####线性变换
* $$\begin{equation}
  \left\{
   \begin{aligned} \notag
   \varepsilon_1^{'} &=a_{11}\varepsilon_1+\cdots+a_{n1}\varepsilon_n\\
   \cdots &  \cdots \cdots \\
   \varepsilon_n^{'} &=a_{1n}\varepsilon_1+\cdots+a_{nn}\varepsilon_n
   \end{aligned}
   \right.
  \end{equation}$$
* $$\begin{bmatrix}
    \varepsilon_1^{'}\\
    \cdots \\
    \varepsilon_n^{'}
\end{bmatrix} = 
\begin{bmatrix}
    a_{11} & \cdots & a_{1n}\\
    \vdots & \ddots & \vdots \\
    a_{n1} & \cdots & a_{nn}
\end{bmatrix}
\begin{bmatrix}
    \varepsilon_1\\
    \cdots \\
    \varepsilon_n
\end{bmatrix} = A
\begin{bmatrix}
    \varepsilon_1\\
    \cdots \\
    \varepsilon_n
\end{bmatrix}$$
* 定义元素之间的加法
* 定义元素的数乘
* 矩阵乘法$MN$->对$N$应用$M$变换
* 旋转、缩放、切变（错切：垂直到一般）、反射
![transform1.png-31.8kB][8]
![transform2.png-26.8kB][9]
* 仿射变换、透视变换
![transform3.png-21.5kB][10]
![transform4.png-25.5kB][11]
* [维基：变换矩阵][12]
|矩阵|形式($P,Q$可逆)|意义|
|---|---|---|
|相似矩阵|$A=P^{-1}BP$|不同基上同一个矩阵（线性变换）|
|投影矩阵|$P=\frac{A A^{T}}{A^{T}A}$|空间向量投影|
|伴随矩阵|$[\cdots C_{ji}\cdots]$|两个线性空间直接的变换诱导的对偶空间上的变换|
|置换矩阵||构成一个置换群|
|等价矩阵|$A = PBQ$|B经过有限次初等变换得到A/秩相同|
|合同矩阵|$A = P^{T}BP$|秩同|
|(实）对称矩阵|$A = Q^{-1}\Sigma Q$|Q标准正交|
|正定矩阵|$A = Q^{-1}\Sigma Q \,\,\,\, \lambda_i > 0$||
|可交换矩阵|$AB=BA$|可交换算子群|
|循环矩阵|$[\cdots C_{(i+j) \mod{n+1}}\cdots]$||
|邻接矩阵||图论|
|埃尔米特矩阵|$\overline{a_{ij}} = a_{ji} \quad A = A^H$||
|Hessian矩阵||函数局部曲率|
|Jacobi矩阵|积分测度下多元函数导数|多元向量函数线性逼近，不同基的不变量|
|协方差矩阵|||
|马尔科夫矩阵||状态转移|

#### 相似矩阵
* $$P\vec \varepsilon = P\begin{bmatrix}
    \varepsilon_1\\
    \cdots \\
    \varepsilon_n
\end{bmatrix} = \begin{bmatrix}
    \sigma_1\\
    \cdots \\
    \sigma_n
\end{bmatrix} = \vec \sigma$$
* A,B为同一变换
* $$A = (T(\varepsilon_1),\cdots,T(\varepsilon_n)) \quad, B = (T(\sigma_1),\cdots,T(\sigma_n)) = PA$$
* $$A\vec \varepsilon = P^{-1}B \vec \sigma = P^{-1}BP \vec \varepsilon$$
* 则$P$作基变换，$A$作线性变换，$P^{-1}$作基变换的逆变换，得到在原基上的线性变换$B$
* 特征值相同 $$|A-\lambda E| = |P^{-1}BP - P^{-1}\lambda EP| = |P^{-1}(B-\lambda E) P| = |P^{-1}||B-\lambda E||P| = |B-\lambda E|$$
#####**对角化或SVD分解**
* 若当标准型
* 设λ是矩阵A的特征值
* + 代数重数： λ作为特征多项式根重数
* + - 一个矩阵的某特征值的代数重数----该矩阵Jordan标准型中与该特征值相关的所有Jordan块的阶数之和
* + 几何重数： 与λ相关联的线性独立的特征向量的最大个数
* + dim N(A-λI)--对应零空间的维数
* + - 一个矩阵的某特征值的几何重数----该矩阵Jordan标准型中与该特征值相关联的Jordan块的个数
* ![对角化.jpg-38.8kB][13]
* 对角化/特征值分解
* + $S = [x_1,\cdots,x_n]$ 为特征向量
* + $AS = S\Lambda \Rightarrow A = S\Lambda S^{-1}$
* + $\Lambda$直接反映了矩阵的特征值/特征向量
* + 仅缩放变换
> ![phasegraph_1.png-70.9kB][14]
> ![phasegraph_2.png-70.2kB][15]
> 沿着图中红箭头方向的向量在映射中保持方向不变
* 奇异值分解/SVD分解
* + $A = \mu \Sigma \sigma^T$
* + $A$ 将向量从$\sigma$基映射到$\mu$基并对每个方向进行缩放（奇异值）
* + 维度差->进行投影

####投影矩阵
* 向量$a,b$
* $$a^{T}(b-xa) = 0 \Rightarrow \textrm{proj}_P = ax = \frac{a a^{T}}{a^{T}a}b \Rightarrow P = \frac{a a^{T}}{a^{T}a}$$
* 注意: $a^Ta$是数，$aa^T$是矩阵
* 最小二乘法
* $\min ||Ax-b||_2^2$
* $$A^{T}A \widehat{x} = A^{T}b$$
* + $\vec b \not \in C(A)_{\textrm{列空间}}$
* + 近似投影$ax_0$使得 $a^T(b-ax_0) = 0$
* + $x_0 = (A^TA)^{-1}A^T$（伪逆）
* + 散点拟合直线 $y = a+bx$，有点$(a_i,y_i)$
* + - $C+a_ix = y_i$
* + - $A=[C,a] \qquad b = [y]$ 参数化为矩阵列
* + - 求向量$b$在列空间上的投影
* + - $A^TA\hat{x}=A^Tb$
* ![least square.jpg-13.9kB][16]

####伴随矩阵
* 线性映射的转置 $A \rightarrow A^* : L(U,W) \rightarrow L(W,U)$
* $$A^{*}=\begin{bmatrix}
C_{11} & C_{21} & \cdots & C_{n1} \\
C_{12} & C_{22} & \cdots & C_{n2} \\
\vdots & \vdots & \ddots & \vdots \\
C_{1n} & C_{2n} & \cdots & C_{nn}
\end{bmatrix} (C_{ij} 表示i,j的代数余子式[有符号])$$
* 逆矩阵 $A^{-1} = \frac{A^{*}}{|A|}$
* 特征值 $Ax=\lambda x \Rightarrow A^*Ax = \lambda A^* x \Rightarrow A^* x = \frac{|A|}{\lambda} x$
* 维数: $A_{(n)} \rightarrow A^*_{(n)} \qquad A_{(n-1)} \rightarrow A^*_{(1)} \qquad A_{(<\,n-1)} \rightarrow A^*_{(0)}$
* 奇异矩阵：不可逆，$\det(A) = 0$
* + 退化的线性映射
* + 特征值含有0

####对称矩阵
* 特征向量正交
* 一些相互垂直的投影矩阵的组合
* 谱定理
* + 正定矩阵
* + - 特征值/行列式/主元/$x^TAx>0$
* + - $x^TA^TAx = (Ax)^T (Ax)>0 \Rightarrow A^TA$正定
* + 半正定矩阵

####合同矩阵
+ 同一个双线性形不同基
+ 二次型（矩阵为数）
+ - $f(x) = \sum a_{ii} x_i^2+ \sum a_{mn}x_{m}x_{n}$
+ - $$f(x) = \begin{bmatrix} 
x_1 , x_2 , \cdots , x_n 
\end{bmatrix}
\begin{bmatrix}
a_{11} & a_{21} & \cdots & a_{n1} \\
a_{12} & a_{22} & \cdots & a_{n2} \\
\vdots & \vdots & \ddots & \vdots \\
a_{1n} & a_{2n} & \cdots & a_{nn}
\end{bmatrix}
\begin{bmatrix}
    x_1\\
    \cdots \\
    x_n
\end{bmatrix}$$
+ - $f(x) = X^TAX$
+ - $A$为对称矩阵,$f(x)$是$A$合同变换的产物
+ - 二次型经过线性变换（$X=CY,\,\det(C)\neq 0$）仍为二次型
+ - * $f(x)=X^TAX\overset{X=CY}{=}Y^TC^TACY \overset{B=C^TAC}{=} Y^TBY$
+ - 标准型（仅含二次项）$\Rightarrow$对角化$\Rightarrow f(x) = X^TAX \overset{X=PY}{=} Y^T \Lambda Y (P^TAP = \Lambda)$对角化$\Rightarrow$与对角阵合同为对称阵
+ 惯性定理
> ![ertia.png-112.6kB][17]
> ![ertia2.png-93.6kB][18]
+ - 合同矩阵正负惯性指数相同
+ 二次型形状$\Leftrightarrow$惯性指数
+ ![positive.png-45.2kB][19]
+ - Eg. 椭圆、双曲线
+ 惯性定理另一表述：基变换下二次曲面类型不变
+ - 规范型 $$f(x) = \sum_{i=1}^{p} y_i - \sum_{j=p+1}^{r(\leq n)} y_j$$
+ - * 每个对称矩阵（二次型）合同于对角线上仅由0,1,-1构成的对角矩阵

####循环矩阵
* 分解基本循环矩阵的多项式
* 矩阵可对角化==相似于循环矩阵
> ![cycle_1.png-40kB][20]
> ![cycle_2.png-41.3kB][21]
> ![cycle_3.png-37.6kB][22]
> ![cycle_4.png-19.1kB][23]

####Hess矩阵&Jacobi矩阵
* 多元函数泰勒展开
* + 1次-$\nabla$
* + 2次-Hessian矩阵
* ![taylor.png-2kB][24]

## 2.行列式
* 矩阵的函数
* + 求矩阵特征值
* + 反对称多重线性型
* + 求体积
* 矩阵对应的线性变换前后的面积比（线性放大率）
* 朗斯基行列式

##奇技淫巧总结
![01140022156线代超强总结.pdf_1.Png-62.4kB][25]
![01140022156线代超强总结.pdf_2.Png-80.7kB][26]
![01140022156线代超强总结.pdf_3.Png-82.2kB][27]
![01140022156线代超强总结.pdf_4.Png-93.2kB][28]
![01140022156线代超强总结.pdf_5.Png-28.2kB][29]
![01140022156线代超强总结.pdf_6.Png-60.6kB][30]
![01140022156线代超强总结.pdf_7.Png-80.6kB][31]
![01140022156线代超强总结.pdf_8.Png-58.8kB][32]
![01140022156线代超强总结.pdf_9.Png-70.7kB][33]
![01140022156线代超强总结.pdf_10.Png-76.6kB][34]
![01140022156线代超强总结.pdf_11.Png-67.9kB][35]
![01140022156线代超强总结.pdf_12.Png-53.2kB][36]


  [1]: http://static.zybuluo.com/Airtnp/z8az6g5hnapdlxkrf586u41o/SVD2.jpg
  [2]: http://static.zybuluo.com/Airtnp/4t3ybhzyi9ztu3q8yf8vr1zl/SVD.jpg
  [3]: http://static.zybuluo.com/Airtnp/ov0dbgop0w2xo3h9pwbac3ie/Variation1.png
  [4]: http://static.zybuluo.com/Airtnp/1zf3zk2bpipvslv9ajbeelmr/Variation2.png
  [5]: http://static.zybuluo.com/Airtnp/6b3hpuqbbpjqul5dunq934kr/Differential%20Equation.png
  [6]: http://static.zybuluo.com/Airtnp/tdg7ldu0g3ha2s9w2rbakr0j/Differential%20Equation_2.png
  [7]: http://static.zybuluo.com/Airtnp/hezdat2awindy65lfbctxbgk/Space.png
  [8]: http://static.zybuluo.com/Airtnp/fmv79reonxxlq0mj6wuz6pm5/transform1.png
  [9]: http://static.zybuluo.com/Airtnp/9f0p1doq2ntda22e12xx6o00/transform2.png
  [10]: http://static.zybuluo.com/Airtnp/vhpybxkux3mmdemee8pzah3r/transform3.png
  [11]: http://static.zybuluo.com/Airtnp/rev87sd6qdwdl8eb59paw11y/transform4.png
  [12]: https://zh.wikipedia.org/wiki/%E5%8F%98%E6%8D%A2%E7%9F%A9%E9%98%B5
  [13]: http://static.zybuluo.com/Airtnp/fetf1zbedugkrsu2ortiek92/%E5%AF%B9%E8%A7%92%E5%8C%96.jpg
  [14]: http://static.zybuluo.com/Airtnp/oze4ltbuzfhvt98bgjvr3zb0/phasegraph_1.png
  [15]: http://static.zybuluo.com/Airtnp/v7q0rp52wclrl46c3sc53o9n/phasegraph_2.png
  [16]: http://static.zybuluo.com/Airtnp/jyxrphgrxsj2oyfluuov3zzd/least%20square.jpg
  [17]: http://static.zybuluo.com/Airtnp/rnnp0lk49won26e6dpzfgpyy/ertia.png
  [18]: http://static.zybuluo.com/Airtnp/jm5fm8k7ap84u9bjtmk0ojcc/ertia2.png
  [19]: http://static.zybuluo.com/Airtnp/llk8kuelerzjjf87yuqs4y5c/positive.png
  [20]: http://static.zybuluo.com/Airtnp/ivxo4tj4jm14cnbvfwrzs1ob/cycle_1.png
  [21]: http://static.zybuluo.com/Airtnp/cghh5y5xnso6c3yxmnta4qrl/cycle_2.png
  [22]: http://static.zybuluo.com/Airtnp/qpbvr4om2xzivj32ao2c0h3b/cycle_3.png
  [23]: http://static.zybuluo.com/Airtnp/ltzfmlzvt4yen8hn32es7r13/cycle_4.png
  [24]: http://static.zybuluo.com/Airtnp/7uoi5ukz91s8j9vr0snqeg7x/taylor.png
  [25]: http://static.zybuluo.com/Airtnp/0ws394pkqjkstfz7bxq9kvcu/01140022156%E7%BA%BF%E4%BB%A3%E8%B6%85%E5%BC%BA%E6%80%BB%E7%BB%93.pdf_1.Png
  [26]: http://static.zybuluo.com/Airtnp/8ksgccyjzcjnyi80j8lhl347/01140022156%E7%BA%BF%E4%BB%A3%E8%B6%85%E5%BC%BA%E6%80%BB%E7%BB%93.pdf_2.Png
  [27]: http://static.zybuluo.com/Airtnp/8hk6pmez6adapneij7oybd0w/01140022156%E7%BA%BF%E4%BB%A3%E8%B6%85%E5%BC%BA%E6%80%BB%E7%BB%93.pdf_3.Png
  [28]: http://static.zybuluo.com/Airtnp/9wcq0ovgvcpnxfcqba6a48s5/01140022156%E7%BA%BF%E4%BB%A3%E8%B6%85%E5%BC%BA%E6%80%BB%E7%BB%93.pdf_4.Png
  [29]: http://static.zybuluo.com/Airtnp/c1ficfwqncwelxwlkwvnk7e5/01140022156%E7%BA%BF%E4%BB%A3%E8%B6%85%E5%BC%BA%E6%80%BB%E7%BB%93.pdf_5.Png
  [30]: http://static.zybuluo.com/Airtnp/knwed1bpuim581d7yn8axkxj/01140022156%E7%BA%BF%E4%BB%A3%E8%B6%85%E5%BC%BA%E6%80%BB%E7%BB%93.pdf_6.Png
  [31]: http://static.zybuluo.com/Airtnp/i9tly431gxo3vn8fka13jalt/01140022156%E7%BA%BF%E4%BB%A3%E8%B6%85%E5%BC%BA%E6%80%BB%E7%BB%93.pdf_7.Png
  [32]: http://static.zybuluo.com/Airtnp/rdg838jxrhg8cgmwx7p3m3tj/01140022156%E7%BA%BF%E4%BB%A3%E8%B6%85%E5%BC%BA%E6%80%BB%E7%BB%93.pdf_8.Png
  [33]: http://static.zybuluo.com/Airtnp/1ms1mcbysp8fopath4feqqst/01140022156%E7%BA%BF%E4%BB%A3%E8%B6%85%E5%BC%BA%E6%80%BB%E7%BB%93.pdf_9.Png
  [34]: http://static.zybuluo.com/Airtnp/wh10mi29bmdvpc0ts8bi1ayu/01140022156%E7%BA%BF%E4%BB%A3%E8%B6%85%E5%BC%BA%E6%80%BB%E7%BB%93.pdf_10.Png
  [35]: http://static.zybuluo.com/Airtnp/ade4n8sm1m86dqqzfjo9ch9k/01140022156%E7%BA%BF%E4%BB%A3%E8%B6%85%E5%BC%BA%E6%80%BB%E7%BB%93.pdf_11.Png
  [36]: http://static.zybuluo.com/Airtnp/9ogzq8y635nm2jfeh1boga89/01140022156%E7%BA%BF%E4%BB%A3%E8%B6%85%E5%BC%BA%E6%80%BB%E7%BB%93.pdf_12.Png