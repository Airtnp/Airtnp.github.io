---
layout:     post
title:      "Multi Variables Calculus Note"
subtitle:   "Too hard"
date:       2016-01-26 20:37:00
author:     "Airtnp"
header-img: "img/post-notes.jpg"
tags:
    - Notes
    - Math
    - Multi Variables
---

---
**$$\int_M d\omega = \oint_{\partial M} \omega$$**


[TOC]

##01

###Vector
* A quantitiy with direction and magnitude of length
* $A = a_i \vec i + a_j \vec j + a_k \vec k = <a_1,a_2,a_3>$
* + Length $|\vec A|$
* + direction $\textrm{dir}{\vec A}$
* + geometric
* + computational/numerical
* **dot product**
* + $\vec A \cdot \vec B = \sum a_i b_i = |\vec A||\vec B|\cos{\theta}$
* + Applications
* + - Length and angle
* + -  judge orthogonality
* plane $x+2y+3z = 0$
* + $\vec A = <1,2,3>$
* + $\vec{OP} = <x,y,z>$
* + $\vec{OP} \cdot \vec {A} = 0$


##02
###Determinant
* $\det{(\vec A, \vec B)} = \begin{vmatrix} a_1 & a_2 \\ b_1 & b_2 \end{vmatrix}$
> $A = LU$
$|A^T| = |A|$等价于证明$|U^TL^T| = |LU|$
等价于证明$|L^T||U^T| = |L||U|$
而L和U都为上(下)三角形式，所以$|L^T| = |L|,|U^T| = |U|$
$\det{(A)} = \det {(A^{T})}$
* $\det{(\vec A, \vec B, \vec C)} = \pm$ volumn on the parallelpipedal
* **Cross Product**
* $\vec A \times \vec B = \begin{vmatrix} \hat{i} & \hat{j} & \hat{k} \\ a_i & a_2 & a_3 \\ b_1 & b_2 & b_3 \end{vmatrix}$
* $|\vec A \times \vec B| =$ area of parallelogram
* $\textrm{dir}(\vec A \times \vec B) \perp$ plane of parallelogram
* $\det{(\vec A , \vec B, \vec C)} = \vec A \cdot (\vec B \times \vec C)$


##03
* Find normal vector $\vec N = \vec{P_1P_2} \times \vec{P_1P_3}$
* triple product $\Leftrightarrow$ determinant
###Matrix
* linear transformation
* The entries in matrices product is dot product of rows of A and columns of B
* ![matrix.png-65.4kB][1]
* $(AB)X$ represents do transformation $B$, then do transformation $A$
* $AB \neq BA$
* Indentity matrix
* + $IX = X = XI$
* Inverse matrix
* + $A^{-1} = \frac{\textrm{adj}{(A)}}{\det{(A)}}$
* Adjacent matrix
* + minors
* + cofactor (with sign)
* + transpose


##04
###Equations of planes/matrices
* P in plane $\Leftrightarrow \vec{OP} \cdot \vec N(<a,b,c>) = 0 \Leftrightarrow ax+by+cz=d$
* constant d means not through origin point
* 2x2 plane equation $\Rightarrow$ a line(basically)
* 3x3 plane equation $\Rightarrow$ a point(basically)
* $A$ is invertible $\Leftrightarrow \det{(A)} \neq 0$
* $\det{(A)} = 0 \Rightarrow \det{(\vec N_1, \vec N_2, \vec N_3)} = 0 \Rightarrow N_1, N_2, N_3$ coplanar
* + 3x3 plane equation $\Rightarrow$ a line


##05
###Parametric Equations
* Equation of lines(intersection of 2 planes)
* trajectory of moving point $\Rightarrow$ parametric equation
* $\vec{Q_0 Q(t)}$
* + **Line**
* + $\vec{Q_0 Q(t)} = \vec{Q_0 Q_1}$
* + **Cycloid**
* + - $\vec{OP} = <a\theta - a\sin{\theta}, a - a\cos{\theta}>$


##06
###Parametric equation
* + Eg. Cycloid
* **direction vector** $\vec r(t)$
* + Eg. $\vec r(t) = <t - \sin{t}, 1-\cos{t}>$
* **velocity vector** $\vec v = \frac{d\vec r}{dt}$
* + Eg. $\vec v(t) = <1-\cos{t}, \sin{t}>$
* **Speed** (scalar) $|\vec v| = |\frac{d\vec r}{dt}| \approx \frac{\Delta \vec r(t+\Delta t) - \Delta \vec r(t)}{\Delta t}$
* + Eg. $|\vec v| = \sqrt{2-2\cos{t}}$
* *Attention*: $|\frac{d\vec r}{dt}| \neq \frac{d|\vec r|}{dt}$
* **Arc length** $s$ distance travelled along trajectory
* + $s = \int |\frac{d\vec r}{dt}| dt = \int |v| dt$
* **Unit tangent vector** $\hat{T} = \frac{\vec v}{|\vec v|}$
* + $\Delta s = \vec r(t+\Delta t) - \vec r(t)$
* + $\Delta \vec r \approx \hat{T} \Delta s$
* Eg. Kepler's second law
* + Motion of planets in a plane
* + The area swept out by the line from the sun to the planet is swept at constant rate
* + Area $\approx \frac{1}{2} |\vec r \times \Delta \vec r| \approx \frac{1}{2} |\vec r \times \vec v| \Delta t$
* + The second law means $|\vec r \times \vec v|$ is constant
* + $\frac{d}{dt}(\vec r \times \vec v) = 0 \Rightarrow \frac{d\vec r}{dt} \times \vec v + \vec r \times \frac{d\vec v}{dt} = 0 \Rightarrow \vec v \times \vec v + \vec r \times \vec a = 0$
* + $\Leftrightarrow \vec r \times \vec a = 0 \Leftrightarrow \vec a // \vec r$
* + $\Leftrightarrow$ Gravitation force // $\vec r$


##07
###Review
* Vector 
* Dot product
* Cross product
* Determinant
* Equation of plane
* + normal vector
* Matrix
* Linear System
* parameters equation


##08
###Function
* $f(x,y) \qquad f(x,y,z)$
* contour plot
* level curve
* $f(x) = f(x_0) + f'(x_0)(x-x_0)+o(x-x_0)$
* partial derivatives
* $\frac{\partial f(x_0,y_0)}{\partial x} = \lim_{\Delta x \rightarrow 0} \frac{f(x_0+\Delta x,y_0)-f(x_0,y_0)}{\Delta x}$


##09
###Function&Partial derivative
* $\frac{\partial f}{\partial x} = f_x$
* $\frac{\partial f}{\partial y} = f_y$
* $\Delta f(x,y) = \Delta z = f_x \Delta x + f_y \Delta y$
* local extreme $\Leftrightarrow$ tangent plane to $z=f(x,y)$ horizonal
* crtical point $f_x(x_0,y_0) = 0 \wedge f_y(x_0,y_0) =0$
* saddle point crtical point not maxima and minima
* least-square $D(a,b)=\sum_{i=1}^{n}[y_i-(ax_i+b)]^2$
* + $\frac{\partial D}{\partial a} = 0 = \sum_{i=1}^{n}2(-x_i)[y_i-(ax_i+b)]$
* + $\frac{\partial D}{\partial b} = 0 = \sum_{i=1}^{n}2(-1)[y_i-(ax_i+b)]$
* + $\sum_{i=1}^{n}(x_i^2a+x_ib-x_iy_i)=0$
* + $\sum_{i=1}^{n}(x_ia+b-y_i)=0$
* + $(\sum_{i=1}^{n} x_i^2)a+(\sum_{i=1}^{n}x_i)b = \sum_{i=1}^{n}x_iy_I$
* + $(\sum_{i=1}^{n}x_i)a+nb = \sum_{i=1}^{n}y_i$
* + 2x2 Linear equation 


##10
###Function's min/max
* global extreme boundary, infinity, crtical point
* $f_{xy} = \frac{\partial f}{\partial x \partial y} = \frac{\partial f}{\partial y \partial x} = f_{yx}$
* Critical point $f_{x_i} = 0 \qquad \prod f_{x_i x_i} - \prod f_{x_i x_j} \neq 0$
* + $A = f_{xx} \,\, B = f_{xy} \,\, C=f_{yy}$
* + $AC-B^2 > 0$ local extreme
* + $AC-B^2 < 0$ saddle point
* + $AC-B^2 = 0$ uncertain
* $\Delta f \approx f_x(x-x_0)+f_y(y-y_0)+\frac{1}{2}[f_{xx}(x-x_0)^2 + f_{yy}(y-y_0)^2+2f_{xy}(x-x_0)(y-y_0)]$
* + So, the critical point have $\Rightarrow w = ax^2+bxy+cy^2 = \frac{1}{4a}[4a^2(x+\frac{b}{2a}y)^2+(4ac-b^2)y^2]$
* + $4ac-b^2>0$ always positive, extreme at origin point
* + $4ac-b^2=0$ saddle point (degenerate critical point)


##11
###Differential
* implicit differentiation
* + $dy = f'(x)dx$
* + $y = F(x) \qquad \frac{d}{dx}(f(x,y) = 0)$
* total differential
* + $df = f_x dx + f_y dy + f_z dz$
* + $\frac{df}{dt} = f_x \frac{dx}{dt} + f_y \frac{dy}{dt} + f_z \frac{dz}{dt}$
* + $$F(x(t),y(t),z(t)) = 0 \Rightarrow \vec T=(x'(t),y'(t),z'(t)) \perp \vec n=(F_x(x_0,y_0,z_0),F_y(x_0,y_0,z_0),F_z(x_0,y_0,z_0))$$
* Chain rule
* + $\frac{dw}{dt} = \frac{dw}{dx}\frac{dx}{dt}$
* + $w=f(x,y) \qquad x=x(u,v) \qquad y=y(u,v)$
* + $dw = f_xdx+f_ydy = f_x(x_udu+x_v dv)+f_y(y_u du + y_v dv)$
* + **Jacobi matrix**
* + - $$J_{f(u_1(x_1,x_2,\cdots,x_n),u_2,\cdots,u_m)} = \begin{bmatrix} 
\frac{\partial u_1}{\partial x_1} & \frac{\partial u_1}{\partial x_2} & \cdots & \frac{\partial u_1}{\partial x_n} \\ 
\frac{\partial u_2}{\partial x_1} & \frac{\partial u_2}{\partial x_2} & \cdots & \frac{\partial u_2}{\partial x_n} \\
\vdots & \vdots & \ddots & \vdots \\
\frac{\partial u_m}{\partial x_1} & \frac{\partial u_m}{\partial x_2} & \cdots & \frac{\partial u_m}{\partial x_n}
\end{bmatrix}$$
* + - $$\begin{bmatrix} du_1 \\ du_2 \\ \vdots \\ du_m \end{bmatrix} = J_f \begin{bmatrix} dx_1 \\ dx_2 \\ \vdots \\ dx_n \end{bmatrix}$$
* + - $$\begin{bmatrix} du_1 & 0 & \cdots & 0 \\0 & du_2 & \cdots & 0 \\ \vdots & \vdots & \ddots & \vdots \\ 0 & 0 & \cdots & du_m \end{bmatrix} = J_f \begin{bmatrix} dx_1 & 0 & \cdots & 0 \\0 & dx_2 & \cdots & 0 \\ \vdots & \vdots & \ddots & \vdots \\ 0 & 0 & \cdots & dx_n \end{bmatrix}$$
* + - $$\prod du_i = |\det{(J_f)}| \prod dx_i = |\det{(\frac{\partial u_1,\partial u_2,\cdots,\partial u_m}{\partial x_1,\partial x_2,\cdots,\partial x_n})}| \prod dx_i$$


##12
###Gradient
* $\frac{dw}{dt} = w_x \frac{dx}{dt} + w_y \frac{dy}{dt} + w_z \frac{dz}{dt} = \nabla w \cdot \frac{d\vec r}{dt}$
* $\nabla w = \textrm{<}w_x,w_y,w_z\textrm{>}$
* $\vec v = \frac{d\vec r}{dt} = <\frac{dx}{dt},\frac{dy}{dt},\frac{dz}{dt}>$ velocity vector (direction derivative)
* $\nabla w \perp$ level plane $w = c$ ($\nabla w$ is the normal vector of the level plane)
* + $w = c \Rightarrow \frac{dw}{dt} = 0 = \nabla w \cdot \vec v \Rightarrow \nabla w \perp \vec v$ (any velocity vector (tangent to level plane))
* direction of $\nabla w$ represent the steepest descent(ascent) direction
* $|\nabla w|$ the directional derivative in that direction
* $\nabla w$ point to the higher value of $w$
* tangent plane $\nabla w \cdot <x-x_0,y-y_0,z-z_0> = 0$
![F(x,y)=−((cosx)^2_+_(cosy)^2)^2.png-68.5kB][2]
###Directional derivative
+ $\frac{dw}{ds} |_{\hat{u}}$
* + direction vector  $\vec r(s),\, \frac{d\vec r}{ds} = \hat{u}$
* + slope of slice of graph by a vertical plane // $\hat{u}$
* + $\frac{dw}{ds} |_{\hat{u}} = \nabla w \cdot \hat{u}$
![Geometrical_interpretation_of_a_directional_derivative.svg-11.9kB][3]


##13
###Lagrange Multipliers
* $f(x,y,z)$ with $g(x,y,z)=c$
* extreme at level curve of $f$ and level curve of $g$ is tangent
* + This conveys $\nabla f$ // $\nabla g \Leftrightarrow \nabla f = \lambda \nabla g$
* $\begin{cases}
f_x = \lambda g_x& \\
f_y = \lambda g_y& \\
\cdots = \cdots\\
g = c\end{cases}$
* At constrained min/max, in any direction along level $g=c$ the rate of change of f must be zero
* For any $\hat{u}$ tangent to $g=c$, $\nabla f \cdot \hat{u} = \frac{df}{ds}|_{\hat{u}} = 0 \Rightarrow \nabla f \perp$ any such $\hat{u}$
* So $\nabla f \perp$ level set of g
* Known $\nabla f \perp$ level set of g
* So $\nabla f  // \nabla g$


##14
###Non-independent variables
* If we view $x^2+yz+z^3 = 8 $ as $z=z(x,y)$
* $2xdx+zdy+(y+3z^2)dz = 0 \Rightarrow \frac{\partial z}{\partial x} ,\, \frac{\partial z}{\partial y}$ as certain point
* $g(x,y,z)=c$ then $dg = g_xdx+g_ydy+g_zdz = 0$
* $dz = \frac{-g_x}{g_z} dx \quad \frac{\partial z}{\partial x} = \frac{-g_x}{g_z} $
* + **Attention**: the variables must be independent
* + $x = u \quad y = u+v$, $(\frac{\partial f}{\partial x})_y \neq (\frac{\partial f}{\partial x})_v = (\frac{\partial f}{\partial u})_v$ 
* + The footnote means which variables to be constant
* Chain Rule


##15
###Review
###Partial differential equation
* Heat equation $\frac{\partial f}{\partial t} = k(\frac{\partial^2 f}{\partial x^2}+\frac{\partial^2 f}{\partial y^2}+\frac{\partial^2 f}{\partial z^2})$
* the solution $f(x,y,z,t)$ is the temperature at $x,y,z$


##16
###Double Integral
* volumn below graph $z = f(x,y)$ over a region R in xy-plane
* Cut R into small pieces of $\Delta A_i$
* $$\iint_R f(x,y) dA = \lim_{\Delta A_i \rightarrow 0}\sum_i f(x_i,y_i) \Delta A_i$$
* $\iint_R f(x,y) dA = \int_{x_{min}}^{x_{max}} S(x) dx$
* $S(x) = \int_{y_{min}}^{y_{max}} f(x,y) dy$
* $\iint_R f(x,y) dA = \int_{x_{min}}^{x_{max}} \int_{y_{min}}^{y_{max}} f(x,y) dy dx$
* $x,\,y$ is non-independent variables, $y = g(x)$
* Exchange the order of integral


##17
###Double Integral on polar coordinate
* $z = f(r,\theta)$
* $x = r\cos{\theta} \quad y = r\sin{\theta}$
* $\iint f(x,y) dxdy = \iint f(r,\theta) \frac{(\partial x,\partial y)}{(\partial r,\partial \theta)} drd\theta$
* $dxdy = \begin{vmatrix} \cos{\theta} & -r\sin{\theta} \\ \sin{\theta} & r\cos{\theta} \end{vmatrix} drd\theta = r dr d\theta$
* $dA$ now means $(r \rightarrow r+\Delta r, \theta \rightarrow \theta + \Delta \theta) = \Delta r\cdot r \cdot \Delta \theta$
* center of mass
* density
* moment of inertia $\sum m_i r_i^2 = \int (x_r^2 + y_r^2) dxdy$
* + ![inertia.jpg-34.9kB][4]
* + $E = \frac{1}{2} m(\omega r)^2 = \frac{1}{2}K \omega^2$


##18
###Change of variables
* **Jacobi matrix**
* - $(u_1,\cdots,u_m) \Rightarrow (x_1,\cdots,x_n)$
* - $$J_{f(u_1(x_1,x_2,\cdots,x_n),u_2,\cdots,u_m)} = \begin{bmatrix} 
\frac{\partial u_1}{\partial x_1} & \frac{\partial u_1}{\partial x_2} & \cdots & \frac{\partial u_1}{\partial x_n} \\ 
\frac{\partial u_2}{\partial x_1} & \frac{\partial u_2}{\partial x_2} & \cdots & \frac{\partial u_2}{\partial x_n} \\
\vdots & \vdots & \ddots & \vdots \\
\frac{\partial u_m}{\partial x_1} & \frac{\partial u_m}{\partial x_2} & \cdots & \frac{\partial u_m}{\partial x_n}
\end{bmatrix}$$
* - $$\begin{bmatrix} du_1 \\ du_2 \\ \vdots \\ du_m \end{bmatrix} = J_f \begin{bmatrix} dx_1 \\ dx_2 \\ \vdots \\ dx_n \end{bmatrix}$$
* - $$\begin{bmatrix} du_1 & 0 & \cdots & 0 \\0 & du_2 & \cdots & 0 \\ \vdots & \vdots & \ddots & \vdots \\ 0 & 0 & \cdots & du_m \end{bmatrix} = J_f \begin{bmatrix} dx_1 & 0 & \cdots & 0 \\0 & dx_2 & \cdots & 0 \\ \vdots & \vdots & \ddots & \vdots \\ 0 & 0 & \cdots & dx_n \end{bmatrix}$$
* - $$\prod du_i = |\det{(J_f)}| \prod dx_i = |\det{(\frac{\partial u_1,\partial u_2,\cdots,\partial u_m}{\partial x_1,\partial x_2,\cdots,\partial x_n})}| \prod dx_i$$
* - $$\int y \prod_i du_i = \int y \cdot |J_f| \prod_i dx_i$$
* **Attention** : $m \neq n$ have linear-dependent variables or have no solution
* $\Delta u \approx \sum_i u_{x_i} dx_i$ 


##19
###Line Integral for Vector Field
* Vector field on xy-plane
* + $\vec F = M(x,y)\vec i + N(x,y)\vec j$
* + Fluid speed at each point (x,y)
* Work and line integrals
* + $$W = \vec F \cdot \Delta \vec r = \int_C \vec F \cdot d \vec r = \lim_{\Delta r_i \rightarrow 0} \sum_i \vec F \cdot \Delta \vec r_i$$
* + $1^{st}$ $$= \sum_i \vec F \cdot (\frac{\Delta \vec r}{\Delta t} \Delta t) = \int_{t_1}^{t_2} \vec F \cdot \frac{d\vec r}{dt} dt$$
* + $2^{nd}$ $$= \int_C (M dx + N dy) = \int_C \vec F \cdot \hat{T} ds$$
* + depend on trajectory but not on parameterization
* + $d\vec r =<dx,dy> = \hat{T} ds$ tangent vector times arc length element
* + ![line_integral.jpg-4kB][5]
* + ![Line_integral_of_scalar_field.gif-580.3kB][6]


##20
###Path-Independent & Conservative Field
* Prerequisite: $\vec F = \nabla f$ (gradient of $f(x,y)$, the potential)
* Fundamental theorem of calculus for line integral
* + $\int_C \vec F \cdot d\vec r = \int_C \nabla f \cdot d \vec r = f(P_1)-f(P_0)$
* + - $x = x(t) \quad dx = x'(t)dt$
* + - $\int_C \nabla f d\vec r = \int_C(f_x \frac{dx}{dt} + f_y \frac{dy}{dt}) dt = \int \frac{df}{dt} dt$
* + **Path-independent**
* + $\vec F = \nabla f$ is conservative (no source potential)
* + close curve $\int_C \vec F \cdot d \vec r = 0$
* Equivalnet properies
* + (1) $\vec F$ is conservative
* + (2) $\vec F$ is path-independent
* + (3) $\vec F = \nabla f$
* + (4) $Mdx+Ndy = df$


##21
###Gradient Field & Potential Function
* $M = f_x \,\, N=f_y$
* $f_{xy}=f_{yx} \Rightarrow M_y=N_x$
* + $\textrm{curl}(\vec F) = 0$
* Path independent-Any path(rectangle/direct)
* Find potential function 
* + 1.use more path
* + 2.use anti-derivative $\int M dx+ g(y)$
* $\vec F$ definition
* + entire plane
* + simply-connected region
###curl
* $\textrm{curl}(\vec F) = N_x-M_y$
* curl measures rotation component of motion
* + the vorticity of motion
* curl measures twice the angular velocity of the rotation component
* curl of a force field measures the torque exerted on a test-object
* $\frac{\textrm{torque}}{\textrm{moment of inertia}} = \frac{d}{dt} (\textrm{angular velocity})$

##22
###Curl
* $\vec F = <M,N>$
* curl($\vec F$) = $N_x - M_y$
###Green's Theorem
* For line integral
* $C$ closed counterclockwise curve enclosing region $R$
* $\vec F$ vector field defined & differentiable in $R$
* then $$\oint \vec F \cdot d \vec r = \iint_R \textrm{curl} (\vec F) d A$$
* $$\oint_C (Mdx+Ndy) = \iint_R (N_x-M_y) dA$$
* Green theorem in *tangent* form
![microscopic_circulation_region_hole.png-30.8kB][7]
* Prove: 
* + first to prove $\oint_C Mdx = \iint_R -M_y dA$
* + decompost $R$ into simpler regions (the connected part will cancel each other)
* + we have $R$ vertically simple
![300px-Green's-theorem-simple-region.svg.png-12.9kB][8]
* + $C$ boundart of $R$ and counterclockwise
* + $\int_{C_{1/3}} M dx = (1/-1)\int_a^b M(x,f_{1/3}(x)) dx \quad [y = f_{1/3}(x) \,\, x(a\rightarrow b)]$
* + $\int_{C_{2/4}} M(x,y)dx = 0 \quad [x = b]$
* + In general, $\oint_C Mdx = \int_a^b M(x,f_1(x)-M(x,f_3(x)) dx$
* + $\iint_R -M_y dA = -\int_{a}^{b} \int_{f_1(x)}^{f_2(x)} \frac{\partial M}{\partial y} dydx = \int_a^b M(x,f_1(x)-M(x,f_3(x)) dx = \oint_C Mdx$


##23
###Flux
* $\int_C \vec F \cdot \hat{n} ds$
* ![400px-General_flux_diagram.svg.png-40.8kB][9]
* Flux = $\lim_{\Delta s \rightarrow 0} (\sum \vec F \cdot \hat{n} \Delta s) = \int_C \vec F \cdot \hat{n} ds$ 
* + *dot product normal vector*
* Work = $\int_C \vec F \cdot d\vec r = \int_C \vec F \cdot \hat{T} ds$ 
* + *dot product tangent vector*
![Flux.jpg-58kB][10]
* calculationusing components
* + $d\vec r = \hat{T} ds = <dx,dy>$
* + by rotated clockwise $90^o$ $\hat{n}ds = <dy,-dx>$
* + $\int_C \vec F \cdot \hat{n} ds = \int_C <P,Q>\cdot<dy,-dx> = \int_C (-Qdx+Pdy)$
* Green's Theorem for flux
* + $C$ encloses $R$ counterclockwisely
* + $\vec F$ defined everywhere
* + $\oint_C \vec F \cdot \hat{n} ds = \iint_R \textrm{div} (\vec F) dA$
* + divergence $\textrm{div}<P,Q> = P_x+Q_y$
* Green theorem in *normal* form
* Prove: 
* + to prove $\oint_C (-Qdx+Pdy) = \iint_R(P_x+Q_y)$
* + let $M = -Q \,\, N = P$
* + $\oint_C Mdx+Ndy = \iint_R(N_x-M_y)dA$
* Interpretation of div$\vec F$
* + rotation/move do not affect
* + measure how much the flow is expanding areas to occupied
* + source in-out
* + new fluid pumped into the system
![curl_div1.jpg-188.3kB][11]
![curl_div2.jpg-200.1kB][12]


##24
###Simply Connected Region
* Validality of Green's Theorem
* + $\vec F$(and derivative) defined everywhere in $R$
* + for origin in curve not apply
* + Need simply connected
* Extended Green's Theorem
* + ![hole_green.jpg-64.5kB][13]
* Simply Connected
* + Definition
* + - a connected region $R$ in the place is simply connected if the interior of any close curve in $R is also contained in $R$
* Review


##25
###Triple integral
* $\iiint_R f dV = \iiint_R f dxdydz$

###Cartesian & Cylindrical Coordinate
* $dz\,dx\,dy = r\, dz \,dr\,d\theta$
* Cylindrical $(r,\theta,z)$
* moment of Inertia in xyz-coordinate

##26
###Spherical Coordinate
* $(\varrho_{\textrm{distance from origin}},\phi_{\textrm{vertical plane to z axis}},\theta_{\textrm{vertical plane to x axis}})$
* ![Spherical_polar_coordinates.PNG-95kB][14]
* $x = r\cos{\theta}=\varrho \sin{\phi}\cos{\theta}$
* $y = r\sin{\theta}=\varrho \sin{\phi}\sin{\theta}$
* $z = \varrho \cos{\phi}$
* $\Delta S \approx a\sin{\phi}\Delta \theta a \Delta \phi = a^2 \sin{\phi} \Delta \phi \Delta \theta$
* $dV = \varrho^2 \sin{\phi} d \varrho d\phi d\theta$
* ![Triple int 2.png-90.7kB][15]

##27
###Vector Field in Space
* Flux in space
* + vector field $\vec F$ surface S
* + orientation for surface
* + Flux = $\iint_S \vec F \cdot d \vec S = \iint_S \vec f \cdot \hat{n} dS$
* + amount of matter through the surface per unit time
###Surface Integral
* $S$ graph of $z = f(x,y)$ $\Rightarrow \hat{n}dS = \pm <-f_x,-f_y,1> dxdy$
![divergence.jpg-34.6kB][16]
* $\vec U = <\Delta x,0,f(x+\Delta x,y)-f(x,y)(=\Delta x \cdot f_x)>$
* $\vec V = <0,\Delta y,f(x,y+\Delta y)-f(x,y)(=\Delta y \cdot f_y)>$
* $\hat{n} \Delta S = \vec U \times \vec V = \begin{vmatrix} \hat{i} & \hat{j} & \hat{k} \\ 1 & 0 & f_x \\ 0 & 1 & f_y \end{vmatrix} \Delta x \Delta y = <-f_x,-f_y,1>\Delta x \Delta y$
![surfaceIntegral1.png-87.9kB][17]
![surfaceIntegral2.png-101.7kB][18]
![surfaceIntegral3.png-31.3kB][19]
![surfaceIntegral4.png-114.6kB][20]
![surfaceIntegral5.png-45.3kB][21]

##28
###Representation of Surface Integral
* **(1)** $S$ graph of $z = f(x,y)$ Can solve z
* + $\hat{n}dS = \pm <-f_x,-f_y,1> dxdy$
* **(2)** $<x,y,z> = \vec r = \vec r(u,v)$ Can parametriic equation

* + $S = \bigg\{\begin{align} x  = x(u,v) \notag \\ y = y(u,v) \notag \\ z = z(u,v) \notag \end{align} $
* + $\hat{n} \Delta S = (\frac{\partial \vec r}{\partial u} \Delta u) \times (\frac{\partial \vec r}{\partial v} \Delta v) = \pm (\frac{\partial \vec r}{\partial u} \times \frac{\partial \vec r}{\partial v})\Delta u \Delta v$
> 参数方程:
（1）通过额外的变量表现方程，对于二维的曲线，额外变量自然是第三维空间里的曲线。
（2）已知A和B俩切空间和切空间C的变换，求AB俩切空间之间的变换的描述方式。
* **(3)** Projection on plane $A$
* + Normal vector $\vec N = \nabla g \quad S:g(x,y,z)=0$
* + surface $A$ as surface $S$'s projection on xy-plane ( $\hat{k}$ as the normal vector of $A$[xy-plane] )
* + $\Delta A = \Delta S \cos{\alpha}$
* + $\cos{\alpha} = \frac{\vec N \cdot \hat{k}}{|\vec N||\hat{k}|}$
* + $\hat{n}\Delta S = \frac{|\vec N|\hat{n}}{\vec N \cdot \hat{k}}\Delta A = \pm \frac{\vec N}{\vec N \cdot \hat{k}}\Delta A$
* + $\hat{n}dS = \pm \frac{\vec N}{\vec N \cdot \hat{k}} dxdy$
###Divergence Theorem (Gauss-Green Theorem)
* S is closed surface enclosing a region $D$ oriented with $\hat{n}$ outwards and $\vec F$ defined ans differentiable everywhere in $D$
* then $$\iint_{S_{closed}} \vec F \cdot d \vec S = \iiint_D \textrm{div} (\vec F) dV$$
* where $\textrm{div}(P\hat{i} + Q \hat{j} + R \hat{k}) = P_x+Q_y+R_z$
* sources-sinks inside region out = surface out
![diverg26.jpg-24.1kB][22]
![Vector_Field_on_a_Sphere.png-438.6kB][23]

##29
###Divergence Theorem
* $\iint_S <P,Q,R>\hat{n} dS = \iiint_R (P_x+Q_y+P_z) dV$
* $\nabla$ operator $\nabla =  <\frac{\partial}{\partial x_1},\cdots,\frac{\partial}{\partial x_n}>$
* $\nabla f = <\frac{\partial f}{\partial x},\frac{\partial f}{\partial y},\frac{\partial f}{\partial z}$ gradient
* $\nabla \cdot \vec F = <\frac{\partial}{\partial x},\frac{\partial}{\partial y},\frac{\partial}{\partial z}> \cdot <P,Q,R> = \frac{\partial P}{\partial x} + \frac{\partial Q}{\partial y} + \frac{\partial R}{\partial z}$ divergence
* Physical interpretation of $\textrm{div}(\vec F)$
* + $\textrm{div}(\vec F)$ = source rate = amount of fluid generated per volume
* + $$\iint_{S_{closed}} \vec F \cdot d \vec S = \iiint_D \textrm{div} (\vec F) dV$$ = amount of incompressible fluid leaving D per unit time
###Proof of divergence theorem:
* + to prove : $\iint_S <0,0,R> \cdot \hat{n} dS = \iiint_D R_z dV$
* + decompose the region into vertical simple region
* + ![disimple.jpg-20.2kB][24]
* + $\iiint_Q R_z dV = \iint_D \int_{g(x,y)}^{h(x,y)} R_z dz dx dy = \iint_D [R(x,y,h(x,y)-R(x,y,g(x,y)] dxdy$
* + $\iint_{S=\textrm{bottom+top+side}} <0,0,R>\hat{n} dS$
* + - $z = g(x,y) \Rightarrow \hat{n}dS = <-\frac{\partial g}{\partial x},-\frac{\partial g}{\partial y},1> dxdy$
* + - $\iint_{\textrm{top}}<0,0,R> \hat{n}dS = \iint_D R(x,y,h(x,y)) dxdy$
* + - the orientated direction of normal vector of top and bottom is reversed
* + - $\iint_{\textrm{side}} <0,0,R> \cdot \hat{n} dS = 0$
* + - * $<0,0,R>$ only have z component, vertical to $\hat{n}$ 
###Diffusion Equation / Heat Equation in immobile medium
* + $u$ concentration at a given point $u(x,y,z,t)$
* + $\frac{\partial u}{\partial t} = k \nabla^2 u = k \nabla \cdot (\nabla u) = \textrm{div}(\nabla u)$
* + - Laplacian $\Delta = \nabla^2 = \nabla \cdot \nabla = <\frac{\partial^2}{\partial x_1^2},\cdots,\frac{\partial^2}{\partial x_n^2}>$
* + $\vec F$ flow of object directed along $-\nabla u$
* + - $\Rightarrow \vec F  = -k\nabla u$
* + $\iiint_D \textrm{div} (\vec F) dV = \iint_S \vec F \cdot \hat{n} dS = $amount of object through $S$ per unit time = $\frac{d}{dt} (\iiint_D u dV) = - \iiint_D \frac{\partial u}{\partial t} dV$
* + - $\Rightarrow \textrm{div} \vec F = - \frac{\partial u}{\partial t}$

##30
###Line integral in space
* $\vec F = P\hat{i}+Q\hat{j}+R\hat{k}$
* $\int_C \vec F \cdot d\vec r = \int_C Pdx+Qdy+Rdz$
* Evaluate by parameterize C
* Test gradient field(total differential/original function) $P_y = Q_x \quad P_z = R_x \quad Q_z = R_y$
![LineIntegral1.png-95.5kB][25]
![LineIntegral2.png-96.7kB][26]
![LineIntegral3.png-74.6kB][27]
![LineIntegral4.png-142.2kB][28]
![LineIntegral5.png-73.8kB][29]
![LineIntegral6.png-79.7kB][30]
###Curl in space
* $\textrm{curl}$($\vec F$) $=(R_y-Q_z)\hat{i} + (P_z-R_x)\hat{j} + (Q_x-P_y) \hat{k}$
* $\textrm{curl}$($\vec F$) $=\nabla \times \vec F = \begin{vmatrix} \hat{i} & \hat{j} & \hat{k} \\ \frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z} \\ P & Q & R \end{vmatrix}$
* rotation component in a velocity field
* + around z-axis
* + - $\vec v = <-\omega y,\omega x,0> \quad \textrm{curl}(\vec v) = 2\omega \hat{k}$
![curl_vector_field_sphere_vector.png-52.2kB][31]

##31
###Stoke's Theorem
* C closed curve, S any surface bounded by C
* $\oint_C \vec F \cdot d \vec r = \iint_S (\nabla \times \vec F ) \cdot \hat{n} dS$
* $$\int_M d\omega = \oint_{\partial M} \omega$$
* right-hand rule along C positively
![stokes.jpg-57.8kB][32]
* Proof:
* + Green Theorem C,S for any plane
* + work, flux, curl exists independent of the coordinates
* + ![stokes2.png-20.3kB][33]
* + cut into tiny flat pieces
* + ![Stokes Theorem.jpg-39.6kB][34]

##32
###Stokes and Path-Independdence
* Simply connected region
* + if every closed loop inside this region bounds some surface again inside this region
* + Space without origin is simply-connected
* + Space without z-axis is not simply-connected
* + Prove by topology
* If $\vec F$ defined in a simply-connected region and $\textrm{curl}(\vec F) = 0$ then $\vec F$ is a gradient, $\int_C \vec F \cdot d \vec r$ is path-independent
* + Proof: Find $S = C_1+C_2$ closed (simply connected)
* + - $\int_{C_1} \vec F d\vec r - \int_{C_2} \vec F d \vec r = \oint_C \vec F \cdot d \vec r = \iint_S \textrm{curl}(\vec F) \hat{n}dS = 0$
* Mobius strip
* + non-orientable surface
* + using surface bounded by mobius strip to orient
* $\iint_{S_1} (\nabla \times \vec F)\hat{n}dS - \iint_{S_2} = \iint_S (\nabla \times \vec F)\hat{n}dS = \iiint_D \textrm{div}(\nabla \times \vec F) dV = 0$
* + $\textrm{div}(\nabla \times \vec F) = (R_y-Q_z)_x + (P_z-R_x)_y+(Q_x-P_y)_z = 0$
###Review
![integrals.png-26.6kB][35]
![integral2.png-11.5kB][36]
![integral3.png-16.8kB][37]
![integral4.png-11.2kB][38]
* Across dimensions
$$\int_M d\omega = \oint_{\partial M} \omega$$

##33
###Maxwell's Equations
* $\textrm{div}(\vec E)$ is constant (derived from **Divergence Theorem**)
* + *Application* $$\iint_S \vec E \cdot d\vec S = \iiint_D \textrm{div} (\vec E) dV = \frac{1}{\varepsilon_0}\iiint_D \varrho dV = \frac{q}{\varepsilon_0}$$
* $\textrm{curl}(\vec E) = -\frac{\partial \vec B}{\partial t}$ (derived from **Stoke's Theorem**)
* + *Application* $$\oint_C \vec E d\vec r = \iint_S (\nabla \times \vec E) d\vec S = \iint_S (-\frac{\partial \vec B}{\partial t}) d\vec S$$
* $\textrm{div}(\vec B) = 0$
* $\textrm{curl}(\vec B) = \mu_0 \vec J + \varepsilon_0\mu_0 \frac{\partial \vec E}{\partial t}$
![Maxwell_1.png-20.4kB][39]
![Maxwell_2.png-19kB][40]
![Maxwell_3.png-12.5kB][41]
![Maxwell_4.png-19.7kB][42]
###Force and Potential
* $\vec F$ derived from potential $\Rightarrow \textrm{\vec F} = 0 \Rightarrow \vec F$ induce no rotation motion

##34
###Review



##35
###Review
* That's the end
* 2016-1-26 20:36


  [1]: http://static.zybuluo.com/Airtnp/6anej95jpma3n53xfrvwfe6t/matrix.png
  [2]: http://static.zybuluo.com/Airtnp/xmaecdgc6gih9tmtg391lmnr/F%28x,y%29=%E2%88%92%28%28cosx%29%5E2_+_%28cosy%29%5E2%29%5E2.png
  [3]: http://static.zybuluo.com/Airtnp/3g09we2d54q6vatpvj7v10l2/Geometrical_interpretation_of_a_directional_derivative.svg
  [4]: http://static.zybuluo.com/Airtnp/lepxkzwh10yamca14v448rhd/inertia.jpg
  [5]: http://static.zybuluo.com/Airtnp/a8ff8yl3is1g1fyo8m34owf3/line_integral.jpg
  [6]: http://static.zybuluo.com/Airtnp/c6das2md1xmbidxgnrf64xwa/Line_integral_of_scalar_field.gif
  [7]: http://static.zybuluo.com/Airtnp/0gnqbdgnnk997e3gjr9nwk3p/microscopic_circulation_region_hole.png
  [8]: http://static.zybuluo.com/Airtnp/6napoapnnf281hlsrhe7jg8k/300px-Green%27s-theorem-simple-region.svg.png
  [9]: http://static.zybuluo.com/Airtnp/03ss69yccjnvk3ank61jef6y/400px-General_flux_diagram.svg.png
  [10]: http://static.zybuluo.com/Airtnp/ml4crltw4sj08h2nbnnixziq/Flux.jpg
  [11]: http://static.zybuluo.com/Airtnp/rwo8kynlua6m4e2f7qm5c2qx/curl_div1.jpg
  [12]: http://static.zybuluo.com/Airtnp/kcd987fcsk35idtuqu174ltx/curl_div2.jpg
  [13]: http://static.zybuluo.com/Airtnp/cw6z4vuv3svuu2ttmxdb9boc/hole_green.jpg
  [14]: http://static.zybuluo.com/Airtnp/2m0e07a3o5w0xowtki02pthm/Spherical_polar_coordinates.PNG
  [15]: http://static.zybuluo.com/Airtnp/70hnwp8wqt6qcv7fyv5pkwb9/Triple%20int%202.png
  [16]: http://static.zybuluo.com/Airtnp/2gy9xjljm14oqy46zca1235v/divergence.jpg
  [17]: http://static.zybuluo.com/Airtnp/a421z10gbwzul9v23iryhi3p/surfaceIntegral1.png
  [18]: http://static.zybuluo.com/Airtnp/9lzpmplr89j6lpiiar4bd7em/surfaceIntegral2.png
  [19]: http://static.zybuluo.com/Airtnp/r9fvdlh98njc0lggqnb9m6s1/surfaceIntegral3.png
  [20]: http://static.zybuluo.com/Airtnp/hscx9c3nfcx334nnb6gpm8cz/surfaceIntegral4.png
  [21]: http://static.zybuluo.com/Airtnp/mslelibb9svo8w8hmmogxpez/surfaceIntegral5.png
  [22]: http://static.zybuluo.com/Airtnp/pvza2c21btaiwxe5lztghpf3/diverg26.jpg
  [23]: http://static.zybuluo.com/Airtnp/1pbn9lt2b4j9k9ip2usr36ax/Vector_Field_on_a_Sphere.png
  [24]: http://static.zybuluo.com/Airtnp/pkj4nuhqhc39pzqkh1e4uldn/disimple.jpg
  [25]: http://static.zybuluo.com/Airtnp/b3g6816o177ney88m3un393k/LineIntegral1.png
  [26]: http://static.zybuluo.com/Airtnp/fvgr20g205hfuph65qvb8mls/LineIntegral2.png
  [27]: http://static.zybuluo.com/Airtnp/kw254ujpj779q6524peagl1b/LineIntegral3.png
  [28]: http://static.zybuluo.com/Airtnp/zd6mp1sf4v9a3mjosdk5mwly/LineIntegral4.png
  [29]: http://static.zybuluo.com/Airtnp/hwojy8zj9e1sikq0re4im4lj/LineIntegral5.png
  [30]: http://static.zybuluo.com/Airtnp/cfhhqlgrpwl0nin8zzk4b2ne/LineIntegral6.png
  [31]: http://static.zybuluo.com/Airtnp/0vsmigmjj89d9vbqsnd434gx/curl_vector_field_sphere_vector.png
  [32]: http://static.zybuluo.com/Airtnp/pb9ep56298cnc0h49bdi68xg/stokes.jpg
  [33]: http://static.zybuluo.com/Airtnp/x6rpm8rd5k6yj2pkdftruvy9/stokes2.png
  [34]: http://static.zybuluo.com/Airtnp/bsyl0e9vzft4krz2f1r3u8ep/Stokes%20Theorem.jpg
  [35]: http://static.zybuluo.com/Airtnp/n7llcxikwz6wba1b2ydzazbn/integrals.png
  [36]: http://static.zybuluo.com/Airtnp/0sa5qyoa7bhnnunwd7qklzzu/integral2.png
  [37]: http://static.zybuluo.com/Airtnp/u4gs1g4rc7hk0gy7hp0a7uyi/integral3.png
  [38]: http://static.zybuluo.com/Airtnp/lk560s4ttwjb2yfgj34dzgzq/integral4.png
  [39]: http://static.zybuluo.com/Airtnp/x112agvqnngj5qelnm0uzb8n/Maxwell_1.png
  [40]: http://static.zybuluo.com/Airtnp/xtod0pa5hoy8vxv86p8ehprg/Maxwell_2.png
  [41]: http://static.zybuluo.com/Airtnp/8d78z4xpzg04dkmf0tnms5t1/Maxwell_3.png
  [42]: http://static.zybuluo.com/Airtnp/h1nx8zs6a21rsvcm62q71xje/Maxwell_4.png