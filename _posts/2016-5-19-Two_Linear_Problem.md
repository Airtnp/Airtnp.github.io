---
layout:     post
title:      "Two Linear Algebra Problem"
subtitle:   "Tricky Idea"
date:       2016-05-18 22:03:00
author:     "Airtnp"
header-img: "img/linear.jpg"
tags:
    - Vector
    - Linear Algebra
---

## How to calculate this uncompleted Vandermonde determinant?

[Origin](http://tieba.baidu.com/p/4555950555)

$$\det{A} = \begin{pmatrix} 1 & 1 & 1 & 1 \\ a_1 & a_2 & a_3 & a_4 \\ a_1^2 & a_2^2 & a_3^2 & a_4^2 \\ a_1^4 & a_2^4 & a_3^4 & a_4^4 \end{pmatrix}$$

Solution: Consider this determinant

$$\det{P} = \begin{pmatrix} 1 & 1 & 1 & 1 & 1 \\ a_1 & a_2 & a_3 & a_4 & y \\ a_1^2 & a_2^2 & a_3^2 & a_4^2 & y^2 \\ a_1^3 & a_2^3 & a_3^3 & a_4^3 & y^3 \\ a_1^4 & a_2^4 & a_3^4 & a_4^4 & y^4 \end{pmatrix}$$

This is a complete Vandermonder determinant. So $\det{P} = \prod_{1 \leq j < i \leq n}\limits (x_i-x_j)$, $x_i \in (a_1, a_2, a_3, a_4, y)$.

For this product, we take the coefficient of component which $\deg{y} = 3$, this operation can be seen as a extending of $\det{P}$ on $y_3$, and we get the coefficient is just the $\det{A}$

## How to conduct vector mixed product and triple product?

[Origin](https://www.zhihu.com/question/21928651)

Mixed Product: $\mathbf{a}\cdot(\mathbf{b}\times\mathbf{c}) = (\mathbf{a}\times\mathbf{b})\cdot \mathbf{c} = (\mathbf{c}\times\mathbf{a})\cdot \mathbf{b}$

Triple Product: $\mathbf{a}\times(\mathbf{b}\times\mathbf{c}) = \mathbf{b}(\mathbf{a}\cdot\mathbf{c}) - \mathbf{c}(\mathbf{a}\cdot\mathbf{b})$

### Method 1

Einstein summation:

$$e_{ijk} = \begin{cases} 1 & \text{for i, j, k in order} \\ -1 & \text{for i, j, k in reverse order} \\ 0 & \text{if i, j, k has two of them equal} \end{cases}$$

$$\delta_{rs} = \begin{cases} 1 & \text{for r = s} \\ 0 & \text{for r}\neq\text{s} \end{cases}$$

$$ \begin{aligned}
(\mathbf{a}\times(\mathbf{b}\times\mathbf{c}))_i & = e_{ijk}a_j(\mathbf{b}\times\mathbf{c})_k \\
& = e_{ijk}a_je_{klm}b_lc_m \\
& = (\delta_{il}\delta_{jm} - \delta_{im}\delta_{jl})a_jb_lc_m \\
& = a_mb_ic_m - a_jb_jc_i \\
& = (\mathbf{a} \cdot \mathbf{c})\mathbf{b_i} - (\mathbf{a} \cdot \mathbf{b})\mathbf{c_i}
\end{aligned}$$

(?)
$$ \begin{aligned}
\mathbf{a} \cdot (\mathbf{b} \times \mathbf{c}) & = \delta_{ij} \mathbf{a}_i(\mathbf{b} \times \mathbf{c})_j \\
& = \delta_{ij} \mathbf{a}_i e_{jkl}\mathbf{b}_k \mathbf{c}_l \\
& = \delta_{kp} \mathbf{b} e_{pli} \mathbf{c}_l \mathbf{a}_i$$

### Method 2 Quaternions

$q = a+bi+cj+dk$

 $1=\begin{pmatrix} 1 & 0 \\ 0 & 1\end{pmatrix}$, $i = \begin{pmatrix} \sqrt{-1} & 0 \\ 0 & -\sqrt{-1}\end{pmatrix}$, $j = \begin{pmatrix} 0 & 1 \\ -1 & 0\end{pmatrix}$, $k = \begin{pmatrix} 0 & \sqrt{-1} \\ \sqrt{-1} & 0\end{pmatrix}$

$\Re{q} = \frac{1}{2}(q+\overline{q})$, $\Im{q} = \frac{1}{2}(q-\overline{q})$

$$\begin{aligned}
(x_1, x_2, x_3, x_4)(y_1, y_2, y_3, y_4)  = & (2x_1y_1 - \sum x_iy_i, \\
& x_1y_2+x_2y_1+x_3y_4-x_4y_3, \\
& x_1y_3+x_3y_1+x_2y_4-x_4y_2, \\
& x_1y_4+x_4y_1+x_2y_3-x_3y_2)
\end{aligned}$$

**Property 1**

$ij=k,\, jk=i,\, ki=j;\,ji=-k,kj=-i,ik=-j;i^2=j^2=k^2=ijk=-1$

**Property 2**

$bi+cj+dk \leftrightarrow (b, c, d) \in \mathbb{R}^3$

**Property 3**

Dot product and cross product of $\Im{q}$s is just as vectors

**Property 4**

$q_1\cdot q_2 = -\Re{q_1q_2}$

$q_1 \times q_2 = \Im(q_1q_2)$

**Property 5**

$q_1 \cdot q_2 = -\frac{1}{2}(q_1q_2+q_2q_1)$

$q_1 \times q_2 = \frac{1}{2}[q_1q_2] = \frac{1}{2}(q_1q_2-q_2q_1)$

$q_1q_2 = -q_1\cdot q_2+q_1\times q_2$

**Property 6 (Jacobi Equation)**

$$q_1 \times (q_2 \times q_3) + q_2 \times (q_3 \times q_1) + q_3 \times (q_1 \times q_2) = 0$$

**Property 7**

$\forall q_1, q_2, q_3 \in \Im{\mathbb{H}}$

$$q_1(q_2q_3) = q_1(-q_2\cdot q_3 + q_2 \times q_3) = -q_1\cdot(q_2\times q_3) - q_1(q_2 \cdot q_3) + q_1 \times (q_2 \times q_3)$$

$$(q_1q_2)q_3 = (-q_1\cdot q_2 + q_1 \times q_2)q_3 = -(q_1\times q_2)\cdot q_3 - (q_1 \cdot q_2 )q_3 + (q_1 \times q_2) \times q_3$$

So $\Re{q_1q_2q_3} = \Re{q_1q_2q_3}$, $\Im{q_1q_2q_3} = \Im{q_1q_2q_3}$

$$\Rightarrow q_1\cdot(q_2\times q_3) = q_3 \cdot (q_1 \times q_2)$$

$$\Rightarrow -q_2\times(q_3\times q_1) = q_1\times(q_2\times q_3) + q_3\times(q_1 \times q_2) = q_3 \cdot (q_1 \times q_2) = -(q_2\cdot q_1)q_3 + (q_2 \cdot q_3)q_1$$

$$q_2\times(q_3\times q_1) = (q_2 \cdot q_1)q_3 - (q_2\cdot q_3)q_1$$
