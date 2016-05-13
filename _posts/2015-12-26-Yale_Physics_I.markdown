---
layout:     post
title:      "Yale Physics I Note"
subtitle:   "Too hard"
date:       2015-12-26 00:19:00
author:     "Airtnp"
header-img: "img/post-notes.jpg"
tags:
    - Notes
    - Physics
---


##**01**
###*Newtonian Mechanics*
####Kinematics(运动学)
+ The matter status
####Dynamics
+ The change of matter

$x-t$ picture = particle moving in time
$\bar{v}$ average velocity
$v(t)$ velocity at a given time = $\lim_{\Delta t \rightarrow \infty} \frac{\Delta x}{\Delta t}$

Falling problem
particle has a constant accleration a
=>second derivatives
=> integration by guess(ansatz)
$$v(t) = \frac{1}{2}at^2+C+bt$$
Gravity Falling 
$$y(t) = -\frac{1}{2}gt^2+c+bt$$
Initial Data => Trajectory

$$v^2=v_0^2+2a(x-x_0)$$

Solve everything by equations

Dirac (p for momentum, m for mass)
$$E^2=p^2+m^2$$
$$E = \pm \sqrt{p^2+m^2}$$
Negative energy<=antiparticels
$$\Delta(\frac{v^2}{2}) = a\Delta x$$

####**01 Chapter End.**
---
##**02**
###Multidimensions Analysis
####2 dimension
* x-y plane
* $(||\cdot||_2,+,\cdot)$ vector space
* + zero vector
* + unit vector (basis vector)
* + modulus
* + modify axis(axes)
* + - $\vec i' = \vec i \cos{\varphi} + \vec j \sin{\varphi}$
* + - $\vec j' = -\vec i \sin{\varphi} + \vec j \cos{\varphi}$
* + - $\vec i = \vec i' \cos{\varphi} - \vec j' \sin{\varphi}$
* + - $\vec j = -\vec i' \sin{\varphi} + \vec j' \cos{\varphi}$
* same entity=same arrow\independent of axes
* Invariant
* + length x^2+y^2
* $$\vec \Omega(t) = \vec i x(t) + \vec{j}y(t)$$
* $$\vec \Omega(t+\Delta t) = \vec i x(t+\Delta t) + \vec{j}y(t+\Delta t)$$
* $$\vec v = \lim_{\Delta t \rightarrow 0} \vec i \frac{dx}{dt}+\vec j \frac{dy}{dt}$$
* $$\vec a = \frac{d^2\Omega}{d^2t} = \frac{dx}{dt}$$
* Circle Movement
* + $$\vec{R}(t) = C(\vec i \cos{\omega t} + \vec j \sin{\omega t})$$
* + - $$\omega = \frac{2\pi}{T} = 2\pi f$$
* + - $$v_\mathrm{(tangential)} = \omega \Omega$$ 
* + - $$\vec v = C(-\vec i \omega \sin{\omega t} + \vec j \omega \cos{\omega t})$$
* $$\vec \Omega = \vec \Omega_0 + \vec v_0 t + \frac{1}{2}\vec a t^2$$
* Same as the 1-D situation
* 
####Projectile motion
* $$x = (v_0\cos{\theta})t$$ $$y = (v_0\sin{\theta})t$$
* 



####**02 Chapter End.**
---
##**03**
###Circle movement
* + centripetal acceleration
* + direction in the radial direction
###Newton Three Law (Inertial System/Reference Frame)
* First Law: Law of **Inertia**
* Second Law: $$F_\mathrm{(cause)}=ma_\mathrm{(natural effect)}$$
* Third Law: $$F_{1->2}=F_{2->1}$$
####**03 Chapter End.**
---
##**04**
###Scale of Newtonian Mechanics
* Speed not comparable to light
* Object not very tiny
###Spring Oscillator
* $$x(t)=a\cos{\omega t}+b\sin{\omega t}$$
###Friction
* Force of static friction
* $$F = \mu_s N$$
###The inclined plane
###The loop the loop problem
$$F = m(\frac{v^2}{r}\pm g)$$
####**04 Chapter End.**
---
##**05**
###Law of Conservation of Energy in 1-Dimension
* Change of energy = work done by all the force
* $$\Delta E = \int_{x_1}^{x_2} F(x) dx=G(x)$$
* $$G(x+\Delta x)-G(x) = F(x) \Delta x$$
####**05 Chapter End.**
---
##**06**
###Law of Conservation of Energy in n-Dimension
* 2-D
* + $\frac{\partial f}{\partial x}|_y$ (y constant x changing)
* + $\frac{\partial^2 f}{\partial x \partial y} = \frac{\partial^2 f}{\partial y \partial x}$
$$f(x+\Delta x,y+\Delta y) - f(x,y) =$$
$$f(x + \Delta x,y + \Delta y) -  f(x+\Delta x,y)+f(x+\Delta x,y)-f(x,y)$$
* + $\Delta f = \frac{\partial f}{\partial x}|_{x,y}\Delta x +\frac{\partial f}{\partial y}|_{x+\Delta x,y}\Delta y$
* + $\frac{\partial f}{\partial y}|_{x+\Delta x,y}\Delta y = \frac{\partial f}{\partial y}|_{x,y}\Delta y + \frac{\partial^2 f}{\partial x \partial y}|_{x,y}\Delta x\Delta y$
* $\Delta f = \frac{\partial f}{\partial x}|_{x,y}\Delta x + \frac{\partial f}{\partial y}|_{x,y}\Delta y + \frac{\partial^2 f}{\partial x \partial y}|_{x,y}\Delta x\Delta y$
* Approximately, $\Delta f = \frac{\partial f}{\partial x}|_{y}\Delta x + \frac{\partial f}{\partial y}|_{x}\Delta y$
* **Law of Conservation**
* + $\Delta K  = F_x \Delta x + F_y \Delta y = \Delta W$
* + $\Delta W = \vec F \cdot \vec \Omega$
* Inner product
* + $\vec A\cdot \vec B=|\vec A||\vec B|\cos{\theta<\vec A,\vec B>}$
* + Independent of the observator(reference frame)
* $\Delta K = \int_{\Omega_1}^{\Omega_2} \vec F d \vec \Omega = U(1)-U(2)$ **Wrong**
* Problem: Integral of random force depends on path?
* Cannot define potential energy of any force
* **Conservative Force**
* + Can define the potential energy
* + Integral independent of the path
* + Construct a conservative
* + - Using potential function U(x,y)
* + - $F_x = -\frac{\partial U}{\partial x} \quad F_y = -\frac{\partial U}{\partial y}$
* + - $\Delta U = \frac{\partial U}{\partial x}dx+\frac{\partial U}{\partial y}dy = -\vec F \cdot d\vec \Omega$
* + - $U(1)-U(2)=\int \Delta U = \int \vec F d \vec \Omega$
####**06 Chapter End.**
---
##**07**
###Judge Conservative Force
* If $\frac{\partial F_x}{\partial y} = \frac{\partial F_y}{\partial x}$
* + Gravity
* + Friction
* + Electrostatic Forces
###Kepler Law
* First Law: All planets go around the Sun on an elliptical orbit with the Sun at the focus.
* Second Law: $\frac{dA}{dt}$ constant
* + A(elliptical area coverd in t time)
* Third Law: $\frac{T^2}{a^3}$ constant
* + T(time for planet to go around Sum) a(orbit size)
###Gravititaion Law
* Assume the orbit is circle
* $F = G\frac{Mm}{R^2}$
* $\vec F = -\frac{GMm}{|\vec R|^2}(\frac{\vec R}{|\vec R|})$
* $\vec F = m \vec a = m \frac{d^2\vec \Omega}{dt^2} = -\frac{GMm}{|\vec \Omega|^2}\hat{\Omega}$
* + $\hat{z}$ means $\frac{\vec z}{|\vec z|}$ modulus 1
* + By solving differential equation
* + One condition
* + - $m\frac{v^2}{\Omega} = \frac{GMm}{\Omega^2}$
* + - $\Leftrightarrow v^2r = GM$
* + - * $v = \frac{2\pi r}{T}$
* + - $\frac{T^2}{r^3} = \frac{4\pi^2}{GM}$
* **Attention**: For tiny particles (huge objects seen as pieces)
* **Attention**: The potential basis may change
* **Attention**: For escape $E=\frac{1}{2}mv^2-m\frac{GmM}{R_E^2}R_E = 0$
* + $v^2 = \frac{2GmM}{R_E}$
####**07 Chapter End.**
---
##**08**
###Dynamics of Multibody
* $$\sum_{i = 1}^{n} m_ia_i = \sum_{i = 1}^{n}F_{environment->i}$$
* $M\vec{R}'' = \vec F_e$
* **Center of mass** $X=\frac{\sum m_ix_i}{\sum m_i}$
* - Only External Force (\Internal Force)
* - Symmetric method
* - Integral method(slice, piece, differential element)
* - Using center of mass and mass to replace object
* - Hanging method
* $M\vec{R}'' = \vec F_e$
* + Case **$I$** $\vec F_e \neq 0$
* + Case **$II_a$** $\vec F_e = 0$
* + - $M\vec{R}''$ constant
* + - $F = m \frac{dv}{dt} = \frac{dp}{dt}$
* + **Law of Conservation of Momentum**
* + - Momentum of center of mass is constant
* + - $p_\mathrm{center\,of\,mass} = \sum p_i$ constant
* + Case **$II_b$** $\vec F_e = 0$ $dX=0$ (center of mass is at rest)
* + - complicated (>three-body)
* Collision
* - Totally elastic
* - + Combine Law of Conservation of Energy
####**08 Chapter End.**
---
##**09**
###Physics of Dynamics of Rigid Bodies
* Complete Rigid Body: Distance of points unchanged during motion
* + Translating
* + Rotating
###No Translating Rotation
* Rigid: all part have same angular velocity 
* Rotation Axis in the point
* + 1-D rotation: no rotate
* + 2-D rotation
* + - 1-D translation ($x$) <=> 2-D rotation ($\theta$)
* + - $\theta = f(t)$
* + - $\omega = \frac{d\theta}{dt}$
* + - $\alpha = \frac{d\omega}{dt}$
* + Positive: counterclockwise
* + $K_{(E_k)} = \frac{1}{2} \sum m_iR_i^2\omega^2 = \frac{1}{2}I\omega^2$
* + $I$ : **the moment of inertia** constant for rigid body
|1-D translation|2-D rotation|
|---------------|------------|
|$x$|$\theta = f(t)$|
|$v$|$\theta = f(t)$|
|$a$|$\alpha = \frac{d\omega}{dt}$|
|$m$|$I$ ($kg \cdot m^2$)|
|$p$|$L=I\omega$ (angular momentum)|
|$F = ma$|$\frac{dL}{dt} = I\alpha = FL$ (torque)|
|$\Delta W = F dx$|$\Delta W = \tau d \theta$|
|$E_k = \frac{1}{2}mv^2$|$E_k = \frac{1}{2}I\omega^2$|
* $\Delta W = F \cdot d = \Delta K$
* $\Delta W = FR\Delta \theta = \Delta K = \Delta(\frac{1}{2}I\omega^2)$
* Approximately, set $\alpha$ constant in a short period
* $\Delta K = I\alpha(\Delta \theta)$
* $\Rightarrow FR = I\alpha$
* torque $\tau = \sum F_i R_i \sin{\theta_i}$ (forces should be perpendicular)
* Hinge 
* Disk's moment of inertia: $\frac{M}{\pi R^2}\int_{0}^{R}2\pi RR^2d\theta = \frac{MR^2}{2}$ (concentric rings)
* Rod's moment of inertia: $$I_{(end)} = I_{(center)}+M(\frac{L}{2})^2 (= \frac{ML^2}{3} - \frac{ML^2}{12})$$
####**09 Chapter End.**
---
##**10**
###Rotation
* moment of inertia with respect to a particular point
* $\tau=FR\sin{\theta}$
* **Parallel Axis Theorem**
* + Known: moment of inertia of center
* + $I_{part} = I_{center} + Md_{(part-center)}^2$
* + Proof:
* + - $I = \sum m_i (\vec R_i + \vec d)\cdot(\vec R_i + \vec d)$
* + - $\,\,\,\,\,= \sum m_i R_i^2 + d^2 \sum m_i + 2\vec d \cdot \sum m_i R_i$
* + - + Since $R_i$ means the distance to center
* + - + $2\vec d \cdot \sum m_i R_i = 0$
* + - Thus, $I = \sum m_i (\vec R_i + \vec d)\cdot(\vec R_i + \vec d) = \sum m_i R_i^2 + d^2 \sum m_i = I_{center}+Md^2$
* **System Analysis** (Set the center of mass as relative)
* + $\vec v_i = \vec v_{X} + \vec v_{i}^r$
* + $K_{sys} = \frac{1}{2}\sum m_i v_i^2 = \frac{1}{2}\sum m_i(v^2+(v_i^r)^2+2\vec v \cdot \vec v_i^r)$
* + - $\vec v \sum m_i \vec v_i^r = \vec v \sum \vec p_i = 0$
* + $K_{sys} = \frac{1}{2}Mv^2 + \frac{1}{2} \sum m_i |v_i^r|^2$(= kinetic energy relative to center)
* + $K_{sys} = \frac{1}{2}Mv^2 + K_{rel}$
* + - For rigid body: Rotation (axis pass through center of mass)
* + - $K_{sys} = \frac{1}{2}Mv^2 + \frac{1}{2}I_{cm}\omega^2$
* + - $K = K_{translation} + K_{rotation}$
* + **Rigid body motion (w.r.t. center of mass) = translation + rotation**
* Rolling without slipping for tyre
* + linear velocity connected angular velocity
* + $v = \frac{2\pi R}{T} = 2 \pi f R = \omega R$
* + $K = \frac{1}{2}Mv^2+\frac{1}{2}I\omega^2 = \frac{1}{2}Mv^2+\frac{1}{2}\frac{MR^2}{2}(\frac{v}{R})^2$
* + $K = \frac{3}{4} Mv^2 = \frac{1}{2}(M+\frac{M}{2})R^2\omega^2 = \frac{1}{2}(MR^2+I_{cm})\omega^2$
* + $K = \frac{1}{2} I_{bottom} \omega^2$ (the part of tyre touches the ground)
* + **Translation must have corresponding rotation energy**
* + **Attention: the part of the tyre touches the ground have zero velocity (rotation of bottom + translation of car)**
* + Example: slippery for cylinder, $mgh = \frac{3}{4}mv^2$
* A system that total torques of external forces is 0
* **Law of Conservation of Angular Momentum**
* Angular momentum conserved if \ ($\sum L_i = \sum L_i^{'}$): $\tau_{external} = 0$
####**10 Chapter End.**
---
##**11**
###$\tau = 0$ $\quad \omega = 0$
* still rigid body
* + $\sum \vec F = \vec 0$
* + - center of mass doesn't move, but the whole rigid body may not
* + $\sum \vec \tau = \vec 0$ ($\exists$ point $\Rightarrow \forall$ point)
###3-Dimension Torque (Vector)
* $\vec \tau = \vec R \times \vec F$
* $|\vec \tau| = |\vec R||\vec F|\sin{\theta}$
* $\theta$: the angle between $\vec R$ and $\vec F$
* The direction of $\vec \tau$ , perpendicular to the plane defined by $\vec R$ and $\vec F$
* **Attention: Only 3-D dimension has cross product**
* + Higher dimension, there are more than one perpendicular vector of plane
###Cross Product
* $\vec A \times \vec B = - \vec B \times \vec A$
* $\vec A \times \vec A = 0$
###3-Dimension Angular Momentum (Vector) for particle
* $\vec L = \vec R \times \vec p$
* $\frac{d\vec L}{dt} = \frac{d \vec R}{dt} \times \vec p + \vec R \times \frac{d \vec p}{dt} = \vec v \times \vec p + \vec R \times \vec F$
* + Velocity and momentum are parallel
* $\frac{d\vec L}{dt} = \vec \tau = \vec R \times \vec F$
* Every particle has angular momentum (regardless of motion)
*  $\frac{d\vec L}{dt} = \sum \frac{d\vec L_i}{dt} = \sum \vec \tau_i = \vec \tau_{external} + \vec \tau_{internal}$
*  Angular Momentum Conservation: Forces exert on other body in the line joining two bodies
*  + Gravatition
*  + Electrostatic
*  + Friction
###Gyroscope Model
* Case I: no initial angular momentum
* Case II: have initial angular momentum
* + The original $\vec L$
* + The new $\vec{\Delta L}$ perpendicular to original one
* => precession (no falling)
* $\frac{\Delta L}{\Delta t} = L \frac{\Delta \theta}{\Delta t} = L\omega_p = L \frac{\tau}{L} = L \frac{mgL}{I\omega}$
####**11 Chapter End.**
---
##**12**
###Relativity (Special)
* Event(x,t), velocity u
* First Event
* + me  (x = 0, t = 0)
* + you (x' = 0, t = 0)
* Second Event
####**Newtonian Mechanics**
* $x'=x-ut \quad t' = t$
* $v = \frac{dx}{dt}$ for S
* $w = \frac{dx'}{dt}$ for S'
* => $w = v-u$
* $a = a' = \frac{dv}{dt} = \frac{dw}{dt}$
* $F = F'$
|  physical quantity |Galilean transformation|
|--------|-------|
|$x'$|$x-ut$|
|$t'$|$t$|
|$v'$|$v-u$|
|$a'$|$a$|
|$F'$|$F$|
* All physics phenomenon applies
####Relativity
* principle pf relativity
* + All inertial observators are equivalent w.r.t. all natural laws (Same form of formula)
* + Velocity of light is independent of state of motion of everything
$$\Bigg\{\begin{aligned}
&x' = (x-ut)\gamma\\
&x  = (x'+ut')\gamma\\
&x  = ct\\
&x' = ct'\\
\end{aligned}$$
* => $1 = \gamma^2(1-u^2/c^2)$
|  physical quantity |Lorentz transformation|
|--------|-------|
|$\gamma$|$\frac{1}{\sqrt{1-u^2/c^2}}$|
|$x'$|$\frac{x-ut}{\sqrt{1-u^2/c^2}}$|
|$t'$|$\frac{t-ux/c^2}{\sqrt{1-u^2/c^2}}$|
####**12 Chapter End.**
---
##**13**
Linear transformation
$x'$ = $\frac{x-ut}{\sqrt{1-u^2/c^2}} = \alpha x + \beta u \quad$ ($c^2\alpha^2-\beta^2 = 1$)
$t'$= $\frac{t-ux/c^2}{\sqrt{1-u^2/c^2}}$
$x'$ = $x\cos{\theta} + y \sin{\theta}$
$y'$ = $-y\sin{\theta} + y \cos{\theta}$
Difference of coordinate obey Lorentz transformation
(By the linear properties)
$v = \frac{\Delta x}{\De lta t}$
$w = \frac{\Delta x'}{\Delta t'} = \frac{\Delta x - u\Delta t}{\Delta t-u\frac{\Delta x}{c^2}} = \frac{\frac{\Delta x}{\Delta t} - u}{1-\frac{u}{c^2}\frac{\Delta x}{\Delta t}} = \frac{v-u}{1-\frac{uv}{c^2}}$
$v = \frac{w+u}{1+\frac{uw}{c^2}}$
$\Delta t = 0 \not \Leftrightarrow \Delta t' = 0$
###Twin Paradox
###Length Contraction
####**13 Chapter End.**
---
##**14**
$\Delta t'<0 \Leftarrow \frac{u}{c} > \frac{c\Delta t}{\Delta x} > 1$ 
* A, B reverse with v < c =>no time for light signal from A to B => A $\not \Rightarrow$ B
####ct-x graph
* absolute future
* present
* absolute past
* light cone
* + outside light cone: may in other light cone
* even horizon
####Invariant of space-time coordinate
* $X = (ct,x,y,z) = (x_0,\vec \Omega)$
* $\beta = \frac{u}{c}$
* $x'(y',z')=\frac{x-\beta x}{\sqrt{1-\beta^2}}$
* $ct' = \frac{ct-\beta x}{\sqrt{1-\beta^2}}$
* Space-time interval Invariant
$$x^2(+y^2+z^2)+(ict)^2 = x'^2(+y'^2+z'^2)+(ict')^2$$
* $S^2 = (ct)^2-x^2-y^2-z^2$
* + Within light cone, $S^2 \geq 0$ := time-like separation
> If two events are time-like separated, then an object can travel from the first event to the second event with a velocity v < c. 
Events separated by a time-like interval are always arranged in the same order in time. That is, if an observer O deduces that event A happens before B, then another observer O', moving relative to O, will also come to the same conclusion. There is a before and after. And there is a possibility that that event A will influence event B. (Cause and Effect.) 
In a space-like interval, an object can be present at both events only if it travels at a velocity v>c. 
Since no object with mass can travel at such a speed, the two events are not causally connected. 
Also, there is no particular order between A and B(in time) if they are space-like separated. 
On a spacetime diagram, for time-like events A and B, B will be within the light-cone of A and vice-versa.
For space-like intervals, one event is outside the light-cone of the other.   
Reference: https://www.physicsforums.com/threads/timelike-and-spacelike.195101/

####4 Dimension vector
* $X = (ct,\vec \Omega) = (x_0,x_1,x_2,x_3)$
* $A \cdot B = (ct_A ct_0B - \vec R_A \vec R_B)$
* pseudo-Euclidean space
* $(c\Delta t)^2-(\Delta x)^2$ also invariant of reference
* $(\Delta S)^2 = c \Delta t\sqrt{1-v^2/c^2}$
* For one particle reference: 
* + $\Delta \tau$ time difference of two event
* + $\Delta x = 0$
* + $(\Delta S)^2 = (c \Delta \tau)^2$
* Space time interval(proper time)
* + Time according the particle itself
* + clock run faster in its own reference
* + $dS = cd\tau$
* + $\Delta \tau = \Delta t \sqrt{1-v^2/c^2}$
* + $ \frac{d\tau}{dt} = \sqrt{1-v^2/c^2}$
* 4-position := Position vector
* + $X = (ct,\vec \Omega) = (x_0,x_1,x_2,x_3)$
* 4-velocity := Velocity vector
* + $\frac{\Delta X}{\Delta \tau} = \frac{dX}{dt}\frac{dt}{d\tau} = \frac{1}{\sqrt{1-\beta^2}}(\frac{dx_0}{dt},\frac{d\vec R}{dt})$
* 4-momentum := Momentum vector 
* + $p = m_0V = (\frac{m_0c}{\sqrt{1-\beta^2}},\frac{m_0 \vec v}{\sqrt{1-\beta^2}}) \rightarrow \infty$
* + - $p_0 = \frac{m_0c}{\sqrt{1-v^2/c^2}} = m_0c(1-\frac{v^2}{c^2})^{1/2} $
$= m_0c(1+\frac{v^2}{2c}+\cdots)=m_0c+\frac{1}{2}\frac{mv^2}{c}$
* + - $cp_0 = m_oc^2+\frac{1}{2}m_0v^2+\cdots$
* + - + still object have energy $cp_0 = \frac{m_0c}{\sqrt{1-v^2/c^2}}$
####**14 Chapter End.**
---
##**15**
###Review
* $X = (ct,\vec \Omega) = (x_0,x_1,x_2,x_3)$
* $\gamma = \frac{1}{\sqrt{1-\beta^2}}$
* $x_1' = \frac{x_1-\beta x_0}{\sqrt{1-\beta^2}}$
* $x_0' = \frac{x_0-\beta x_1}{\sqrt{1-\beta^2}}$
* $x \cdot x = x_0^2-x_1^2 = x_0^2-\vec R \cdot \vec R = S^2$
* $\Delta S = \sqrt{(c\Delta t)^2 - (\Delta x)^2}$
* $\Delta S = c\Delta t \sqrt{1-(\frac{\Delta x}{\Delta t})^2\frac{1}{c^2}} = cd\tau$
* $d\tau$: time elapsed according to the particle itself
* $p = m_0V = (\frac{m_0c}{\sqrt{1-\beta^2}},\frac{m_0 \vec v}{\sqrt{1-\beta^2}}) = (\frac{E}{c},\vec p)$
* $P = (p_0,p)$
* $E = mc^2\gamma$
* $\vec p = m\vec v \gamma$
* **Quaternion** $a+bi+cj+dk$ no commutative law
* $P \cdot P = p_0^2-p^2 = m^2c^2$ independent of velocity
* $E^2 = c^2p^2+m^2c^4$
* + photon $E^2 = (cp)^2$
* + photon $K = (\frac{\omega_{energy}}{c},\vec K_{momentum})$ $\quad \omega = kc $ $\quad K\cdot K = 0$
* $P_in = \sum p_i = \sum p_j = P_out$ collision into different number particles
* => $\sum p_i' = \sum p_j'$ for observer
####**15 Chapter End.**
---
##**16**
###Talyor Series
* $$f(x)=\sum_{i = 0}^{\infty} \frac{f^{(i)}(x_0)}{i!}(x-x_0)^i$$
* $ e^{i\pi} + 1 = 0$
###Complex Number
* $z = r(\cos{\theta}+i\sin{\theta}) = re^{i\theta} = x+iy$
* Multiply => Rotation
####**16 Chapter End.**
---
##**17**
###mass block on the string
* restoring force
* $F = -kx = m\frac{d^2 x}{dt^2}$
* $\omega = \sqrt{\frac{k}{m}}$
* $x = A\cos{(\omega t -\varphi)}$
###(?)bar suspended by a cable celling
* restoring torque
* $-\kappa \theta = I \frac{d^2 \theta}{d \theta^2}$
* $\theta = A\cos{(\omega t -\varphi)}$ $\quad \omega = \sqrt{\frac{\kappa}{I}}$
* $\tau = -\kappa \theta$
###Pendulum
* massless rod + mass at bottom + disturbance
* $\tau = -rF\sin{\theta} = -rF\theta = -mgl\theta$
$\frac{d^2x}{dt^2}= \omega_0^2x$ => $x = Ae^{\alpha t}$ => $A(\alpha^2+\omega_0^2)e^{\alpha t} = 0$ => $\alpha = \pm i\omega_0$
* + $x_1(t)  =Ae^{i\omega_0t} \quad x_2(t)  =Be^{-i \omega_0t}$
* + Linear Space of solutions of ODE => superposition
* $x(t) = Ae^{i\omega_0t} \quad x_2(t)  =Be^{-i \omega_0t}$
* Since $x(t) = \overline{x}(t)$ => $B = \bar{A}$
* $x(t) = Ae^{i\omega_0t} +\overline{A}e^{-i \omega_0t}$
####**17 Chapter End.**
---
##**18**
###$mx''+bx'+kx=F_0\cos{\omega t}$
* $x''+\gamma x'+\omega_0 x =(\frac{F_0}{m})\cos{\omega t}$
* $x''+\gamma x'+\omega_0 x =0$
* + Ansatz: $x(t) = Ae^{\alpha t}$
* + $(\alpha^2+\gamma \alpha +\omega_0^2)Ae^{\alpha t} = 0$
* + $\alpha_\pm = \frac{\gamma}{2} \pm \sqrt{(\frac{\gamma}{2})^2-\omega_0^2}$
* + $x = Ae^{-|\alpha_+|t}+\overline{A}e^{-|\overline{\alpha_+}| t} = Ce^\frac{\gamma t}{2} \cos{(\omega t +\varphi)}$
* + damped oscillation
* Inhomogeneous ODE
* $x''+\gamma x'+\omega_0 x =(\frac{F_0}{m})\cos{\omega t} = \frac{F_0}{m}e^{1\omega t}$
* Ansatz: $z = z_0e^{i\omega t}$
* $z_0 = \frac{F_0/m}{-\omega^2+i\omega \gamma +\omega_0^2}$
* Impedance $I(\omega) = -\omega^2+i\omega \gamma +\omega_0^2$
* $z_{part} = \frac{F_0/m}{I(\omega)}e^{i\omega t} = \frac{F_0/m}{|I|}e^{i(\omega t-\varphi)} = \frac{F_0/m}{|I|}\cos{(\omega t -\varphi)}$
* $|I| = \sqrt{(\omega^2-\omega_0^2)^2+\omega^2\gamma^2}$
* + resonance
* $x(t) = x_{hom}+x_{part} = \frac{F_0/m}{|I|}\cos{(\omega t -\varphi)} + Ce^\frac{\gamma t}{2} \cos{(\omega t +\varphi)}$
###Wave
* $\mu$ mass per unit length
* $T$ tension
* $\varphi$ vibration length
* $T sin{(\theta+\Delta \theta)} - T\sin{\theta} = \mu dx \frac{\partial^2 \varphi}{\partial t^2}$
* $\sin{\theta} = \theta = \tan{\theta} = \frac{d\varphi}{dx}$
* Approximately $T \frac{\partial^2 \varphi}{\partial x^2} = \mu \frac{\partial^2 \varphi}{\partial t^2}$
* **Wave Equation**
* + $\frac{\partial^2 \varphi}{\partial x^2} = \frac{1}{v^2}\frac{\partial^2 \varphi}{\partial t^2} \quad v^2 = \frac{T}{\mu}$
* + A particular solution for waves on a string:
* + + $\varphi(x,t) = A\cos{(kx-\omega t)} \quad k =\frac{\omega}{v}$
* + + $\varphi(x,t) = A\cos{(k(x-vt))}$
####**18 Chapter End.**
---
##**19**
###Wave on a string
$\varphi(x,t) = A\cos{(kx-\omega t)} \quad k =\frac{\omega}{v}$
$\varphi = A\cos{(\frac{2\pi x}{\lambda} - \frac{2\pi t}{T})}$
$v= \frac{\omega}{K} = \frac{2\pi}{T} \frac{\lambda}{2\pi} - \frac{\lambda}{T} = \lambda f$
$E = \int \frac{1}{2} \mu  (A\omega)^2 dx$
$P = \frac{1}{2} \mu A^2\omega^2 v$
Intensity $I = \frac{P}{S}$
Decibels $\beta = 10 \log{\frac{I}{I_0}} \quad I_0 = 10^{-12} w/m^2$
####**Doppler Effect**
* Sitting still wavelength: $\lambda$
* Approaching speed u: $\lambda' = \lambda-\frac{u}{f}$
* + $f' = \frac{f}{1-\frac{u}{v}}$
* Leaving speed u: $\lambda''=\lambda+\frac{u}{f}$
* + $f' = \frac{f}{1+\frac{u}{v}}$
####**Superposition of Wave**
* $\varphi = 2A\cos{\frac{\omega_1+\omega_2}{2}t}\cos{\frac{\omega_1+\omega_2}{2}t}$
* Wave overlap
* Wave construction
* Wave destruction
* Length of tube and node relation
####**19 Chapter End.**
---
##**20** 
###Fluid Dynamics and Statics
####Static Fluids
* density $\rho$
* pressure $p = P_0+\rho g h$
* hydraulic press $P_1S_1\Delta x_1=P_2S_2 \Delta x_2$
* Incompressible fluid
* Archimedes Principle
* + weight loss equals weight of liquid displaced
####Dynamic 
* **Bernoulli Equation**
* Incompressible $S_1v_1 = S_2v_2$
* $\Delta P_1+\frac{1}{2}\rho v_1^2+\rho g h_1 = \Delta P_2+\frac{1}{2}\rho v_2^2+\rho g h_2$
####**20 Chapter End.**
---
##**21**
###Thermodynamics
* Equilibrium
* Zeroth Law: If $T_a = T_b,\,T_b=T_c \Rightarrow T_a=T_c$
* + **Celsius**: Sea level water triple point $\Rightarrow$ $℃$
* + **Kelvin**: dilute gas $PV \propto T \Rightarrow$ $K$
* caloric fluid
* + $\Delta Q = c m_{gram} \Delta T \quad$ (unit: calories)
* $\Delta L = \alpha_\textrm{(linear expansion)} L \Delta T$
* phase change
* heat-exchange problem
* heat transfer
* + radiaton
* + convection
* + conduction
* + - $\frac{dQ}{dt} = -\kappa\frac{A \Delta T}{L_{\Delta x}}$
* + - $\kappa$ thermoconductivity
####**21 Chapter End.**
---
##**22**
* $PV = NkT = nRT$
* $R$: Boltzmann Constant $= 1.4 \times 10^{-23} J/K$
* Avogadro's Number $6.2\times 10^{-23}$
* $F = \frac{dp}{dt} = d{mv}{dt} = ma$
* Collision
* + $F_\textrm{one molecule} = \frac{\Delta P}{\Delta t} = \frac{mv-(-mv)}{\frac{2L}{v}}$
* + $F_\textrm{average all} = \frac{N}{3}\frac{mv^2}{L}$
* + $\overline{P}_{average} = \frac{N}{3}\frac{mv^2}{L^3} \Rightarrow PV = \frac{N}{3}mv^2 = NkT$
* + - $\Rightarrow \frac{1}{2}mv^2 = \frac{3}{2}kT$
* Heat solid vibration => change of location => liquid
* Maxwell-Boltzmann distribution
* + $f(v)=v^2e^{-\frac{mv^2}{2kT}}$
###**First Law of Thermodynamics**
* $\Delta U = \Delta Q - \Delta W = \Delta Q - P\Delta v$
* $W_\textrm{gas volume work} = \int P \Delta V = \int \frac{nRT}{V} dV = nRT\ln{\frac{V_2}{V_1}}$
####**22 Chapter End.**
---
##**23**
###**First Law of Thermodynamics**
* Equation of state
* + $PV = nRT$
* P-V graph
* $U = \frac{3}{2}NkT = \frac{3}{2}nRT = \frac{3}{2}PV$
* $\Delta U  =\Delta Q - P dV = \Delta Q -\Delta W$
* Constant Temperature Isothermal Process
* + $W_\textrm{gas volume work} = \int P \Delta V = \int \frac{nRT}{V} dV = nRT\ln{\frac{V_2}{V_1}}$
* $C = \frac{\Delta Q}{\Delta T}$ for mole
* + constant volume
* + - $C_v = \frac{\Delta Q}{\Delta T}|_v = \frac{\Delta U}{\Delta T} = \frac{3}{2}R$ (for ideal gas)
* + constant pressure
* + - $C_p = \frac{\Delta Q}{\Delta T}|_p = C_v + \frac{\Delta pV}{\Delta T} = C_v+R = \frac{5}{2}R$ (for ideal gas)
* $\gamma  = \frac{C_p}{C_v} = \frac{5}{3}$ (for ideal gas)
* In P-V graph a cycle
* + $W_\textrm{cycle} = \oint P dV$
* + $\Delta U_\textrm{cycle} = 0$
* + $W_\textrm{down} = Q_\textrm{in}$
* Isothermal process $\Delta T = 0 \quad PV = C$ (constant)
* Isobaric process $\Delta P$ = 0
* Constant volume process $\Delta V = 0 \quad W = 0$
* Adiabatic process $\Delta Q = 0$
* + $\Delta U + P\Delta V = 0 \Rightarrow nC_v\Delta T + \frac{nRT}{V}\Delta V = 0$
* + $\Rightarrow \frac{C_v}{R} \frac{\Delta T}{T} + \frac{\Delta V}{V}  =0$
* + $\frac{C_v}{R} \int \frac{\Delta T}{T} + \int \frac{\Delta V}{V}  =0 \Rightarrow (\frac{T_2}{T_1})^{\frac{C_v}{R}} \frac{V_2}{V_1} = 1$
* + $(T_1)^{\frac{C_v}{R}}V_2 = (T_2)^{\frac{C_v}{R}}V_1$
* + For ideal gas
* + - $(T_1)^{\frac{3}{2}}V_2 = (T_2)^{\frac{3}{2}}V_1$
* + Or $PV^{\gamma} = c$ (constant)
* + $W = \int P(v) dv = c\int \frac{dV}{V^\gamma} = \frac{V_2^{1-\gamma} - V_1^{1-\gamma}}{1-\gamma} = \frac{P_1V_1-P_2V_2}{\gamma-1}$ 
###**Second Law of Thermodynamics**
* In every real process, $\sum S \nearrow$
* Carrot Law
* + $\eta = \frac{W_\textrm{work}}{W_\textrm{all}} < 1$
* + cannot build a engine whose sole effect is transfer the heat from cold source to hot source
* Carrot Engine
* + A, B in one PV line,   C, D in another PV line
* + $A \rightarrow B \rightarrow C \rightarrow D \rightarrow A$
* ![Carrot Engine.png-145.3kB][1]
* $\eta = 1-\frac{T_2}{T_1}$
####**23 Chapter End.**
---
##**24**
###Carrot Engine
* ![Carrot Engine-2.png-119.2kB][2]
* Carrot Engine is the most effective engine
* ![Carrot Engine-3.png-31.4kB][3]
###Entropy
* $\Delta S = \frac{\Delta Q}{T}$
* $\oint dS = \sum \frac{\Delta Q}{T} = 0$ (state function)
* $\Delta S = \sum \frac{\Delta Q}{T} = \int_{T_1}^{T_2}mC\frac{dT}{T} = mC \ln(\frac{T_\textrm{final}}{T_\textrm{initial}})$ (given mass)
* $\Delta S = \sum \frac{\Delta Q}{T} = \sum \frac{P}{T} dV = \sum nR \frac{\Delta V}{V} = nR\ln{\frac{V_1}{V_2}}$ (given temperature isothermally)
* **Second Law of Thermodynamics**
* + $\Delta S \geq 0$
* **Boltzmann Formula**
* + $S = k\ln{\Omega}$
* + $\Omega$: the number of different microscopic arrangement (though same macroscopicially)
* + $k$: Boltzmann constant
* + As $N \nearrow$ configuration to 50/50 $\Omega = 2^{N}$
* Statistic Law
####**24 Chapter End.**
---


  [1]: http://static.zybuluo.com/Airtnp/wjni48lw9j1hne7183s6qm5b/Carrot%20Engine.png
  [2]: http://static.zybuluo.com/Airtnp/hj4q40tb0evkltvw39qemk5o/Carrot%20Engine-2.png
  [3]: http://static.zybuluo.com/Airtnp/o1lhpxkhgzw4zljlm2y901gr/Carrot%20Engine-3.png