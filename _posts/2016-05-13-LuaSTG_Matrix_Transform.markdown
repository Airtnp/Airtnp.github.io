---
layout:     post
title:      "Matrix Transform for LuaSTG"
subtitle:   "copy from css3"
date:       2016-05-13 22:03:00
author:     "Airtnp"
header-img: "img/post-matrix.jpg"
tags:
    - LuaSTG
    - Linear Algebra
---

<del>Another time copy from css (first attempt is ease function)</del>

## Theory

From css3 animation, we have matrix, matrix3d method to describe transform of a image affinely. 

For 2d image:
0. translate, skew and scale according to (0, 0)

$$\begin{bmatrix} x \\ y \\ 1 \end{bmatrix}  
\begin{bmatrix}
	\text{scaleX} & \text{skewX} & \text{translateX} \\
	\text{skewY} & \text{scaleY} & \text{translateY} \\
	0 & 0 & 1
 \end{bmatrix}$$

0. rotation according to (0, 0)

 $$\begin{bmatrix} 
	\cos{\theta} & -\sin{\theta} & 0 \\
	\sin{\theta} & \cos{\theta} & 0 \\
	0 & 0 & 1
 \end{bmatrix}$$

Matrix is kinda linear transformation, so rotation matrix ($R$) + sketching matrix ($S$) = $T(=RS)$

 If we have matrix $A$ (invertiable), we can use eigenvalue decomposition to tween, $A=VDV^{-1}$, if separated into 10 steps, $T = VD^{1/10}V^{-1}$

 Also for matrix 3d on 2d image:

o. translate, skew and scale according to (0, 0, 0)

$$\begin{bmatrix} x \\ y \\ 1 \end{bmatrix}  
\begin{bmatrix}
	\text{scaleX} & \text{skewX} & \text{translateX} \\
	\text{skewY} & \text{scaleY} & \text{translateY} \\
	\text{skewZ} & \text{translateZ} & \text{scaleZ} \\
	0 & 0 & 1
 \end{bmatrix}$$

o.rotation according to (x, y, z) [rotation](http://blog.csdn.net/harryhare/article/details/9195053) [wiki](https://zh.wikipedia.org/wiki/%E6%97%8B%E8%BD%AC%E7%9F%A9%E9%98%B5)

$$ \mathcal{M}(\hat{\mathbf{v}},\theta) = \begin{bmatrix}
   \cos \theta + (1 - \cos \theta) x^2
 & (1 - \cos \theta) x y - (\sin \theta) z 
 & (1 - \cos \theta) x z + (\sin \theta) y & 0 
\\
   (1 - \cos \theta) y x + (\sin \theta) z 
 & \cos \theta + (1 - \cos \theta) y^2
 & (1 - \cos \theta) y z - (\sin \theta) x & 0
\\
   (1 - \cos \theta) z x - (\sin \theta) y
 & (1 - \cos \theta) z y + (\sin \theta) x
 & \cos \theta + (1 - \cos \theta) z^2 & 0
 \\
 0 & 0 & 0 & 1
\end{bmatrix} $$

Similarily, we can have eigenvalue decomposiiton to make tweening animation. One point is remained that for 3d object projected to xy-plane, we should make parameter equation for each surface.

Finally we can use projection of surface to create beautiful bullets. 

## Realization

Use pyqt as gui, matplotlib.pylab, mpl_toolkits.mplot3d as drawer.
To simplify this problem, we only draw edges of convex polyhedron on xy-plane.

### Place points at anticlockwise direction and add edges

[anticlockwise sort](http://www.cnblogs.com/loveclumsybaby/p/3420795.html)

Calculate the mass center, $\vec{OA}, \vec{OB}$ as vector from mass center to point A, B. If $\vec{OA} \times \vec{OB} < 0$, then B is anticlockwise to A. Quick sort the whole point set. Add edges AB in the edges set

### Solve the convex

Accordint to anticlockwise points set and edges set, judge one edge AB and one point C. If the $CBA < 90^{\circ}$ then it's concave, error.

## Example

Remain to be done