---
layout:     post
title:      "Yale Physics II Note"
subtitle:   "Too hard"
date:       2015-12-28 14:48:00
author:     "Airtnp"
header-img: "img/post-notes.jpg"
tags:
    - Notes
    - Physics
---

##**01**
###Electronstatic
* glass rub on fur
* rubber rub on hair
* **Coulomb's Law**
* + $F = \frac{q_1 q_2}{4\pi \varepsilon_0 R^2} = 9\times 10^9 \frac{q_1q_2}{R^2}$
* Charge is conserved
* Charge is quantized $1.6\times10^{-19} C$
* Charge is local
* Coulomb Force >> Gravitation
* $q_n = 0 \quad q_e = -1.6\times 10^{-19} \quad q_p  = 1.6\times 10^{-19}$
####01 Chapter End.
---
##**02**
###Electric Field
* Charge cause field
* $\vec F = q\vec E \vec i$ ($\vec i$ unit vector)
* $\vec E = \frac{q}{4\pi \varepsilon_0} \frac{1}{R^2}\vec{e_R} = \frac{q\vec R}{4\pi \varepsilon_0 R^3}$
* $\textrm{density of lines} = \frac{\textrm{number of lines cross a surface perpendicularly}}{\textrm{ area of surface}}$
* $(-a,-q) \quad (a,q)$: dipole
* + $\vec E = \vec e \frac{q}{4\pi \varepsilon_0} \frac{4xa}{(x^2-a^2)^2} \approx -\vec e \frac{q2a}{2\pi \varepsilon_0} \frac{1}{x^3} = \frac{\vec e  p}{2\pi \varepsilon_0 x^3}$
* $p = 2aq$ dipole moment of dipole
* two plates problem
* 
####02 Chapter End.
---
##**03**
* Integral on infinite line density $\lambda$ $\vec E  =\frac{\lambda}{2\pi \varepsilon_0 a}$
* Integral on infinite plane density $\sigma$  $\vec E = \frac{\sigma}{2\varepsilon_0}$ (not dependent on distance)
* Integral on solid ball density $\rho$
###Gauss Law
* define vector perpendicular to the area and magnitude = area
* right-hand rule to define direction
* flow rate $\varPhi (m^3/s) = Sv$
* Or flux $\varPhi = \vec v \cdot \vec S$
* $\int \vec E \cdot d \vec S = \int \frac{q}{4\pi\varepsilon_0}\frac{1}{R^2}d S \vec{e_R} \cdot \vec{e_R} = \frac{q}{\varepsilon_0}$
* $\iint_{sphere} \vec E \cdot d \vec S = \frac{q}{\varepsilon_0}$
* Gauss Law: surface enclose a charge
* in surface $$\iint_S \vec E \cdot d \vec S = \frac{\sum q_{inside}}{\varepsilon_0}$$
* $DV$ the boundary of V
* discrete $$\oint_{S = DV} \vec E d \vec S = \frac{q_\textrm{enclose}}{\varepsilon_0}$$
* $\rho$ charge density
* continuous $$\iiint_V \rho(x,y,z) dxdydz $$
* $$\iint_S \vec E \cdot d \vec S = \frac{1}{\varepsilon_0}\iiint_\tau \rho d\tau $$
* $$\nabla \cdot \vec E = \frac{1}{\varepsilon_0}\rho$$
####03 Chapter End.
---
##**04**
###Gauss Law
* Same lines across the surface
* line density $\propto \frac{q}{R^2}$
* electric filed $E(R) \propto \frac{q}{R^2}$
* So line density $= c E(R)$
* $\Phi_S$ number crossing sphere
* $\Phi_S = \textrm{line density} \times \textrm{area of sphere} = cE(R)4\pi R^2$
* $\Phi_S = c\iint \vec{E(R)} \cdot d \vec S$
* So, $\iint \vec{E(R)} \cdot d \vec S = \frac{q}{\varepsilon_0}$
* Gaussian Surface $raidus=R sphere$
* $\vec{E(R)} = \frac{q}{4\pi\varepsilon_0R^2}$
* Cone for hollow sphere
* static shielding
* area integral $\iint r drd\theta f(r,\theta)$
####04 Chapter End.
---
##**05**
###**Work Energy Theorem**
* $\Delta \frac{mv^2}{2} = \int F(x) dx$
* Conservative force $\oint \vec F \cdot d \vec r = 0$
* $U(x,y)$
* + $F_x = -\frac{\partial U}{\partial x} \quad F_y = -\frac{\partial U}{\partial y}$
* $\vec F = \vec x (-\frac{\partial U}{\partial x}) + \vec y (-\frac{\partial U}{\partial y}) = -\vec{\nabla} U$
* All conservative force are of the form $\vec \nabla U$
* $V(\vec R_2)-V(\vec R_1) = -q\int \frac{\vec{e_R}}{4\pi \varepsilon_0} \vec{e_R} d R = \frac{q}{4\pi \varepsilon_0} (\frac{1}{R_2}-\frac{1}{R_1})$
* $\frac{1}{2}mv^2+qV(\vec R_1) = \frac{1}{2}mv^2 + qV(\vec R_2)$
* $V(R) = \frac{1}{4\pi\varepsilon_0} \sum \frac{q_i}{|\vec R_i - \vec R|}$
####05 Chapter End.
---
##**06**
###Advantage of potential V
* conservation of energy
* computation of E
* visual
* $V = -\int \vec E \cdot d \vec R$
###Conductor
* hollow cavitiy/inside the hole no charge
* Every conductor is equipotential
###Capacitor
* $C = \frac{Q}{V}$
* parallel plate
* + $V = Ed = \frac{sigma}{\varepsilon_0}d = \frac{Qd}{S\varepsilon_0} = \frac{Q}{C}$
* + $C = \frac{\varepsilon_0S}{d}$
####06 Chapter End.
---
##**07**
###Conductor
* Equalpotential Real Charge Problem
* surface integral => fake(image/mirror) charge
* inversion
* Uniqueness theorem
* + potential determined by charge distribution + potential of conductors
###Capacitor
* parallel plates $C  =\frac{\varepsilon_0S}{d}$
* $U = \frac{1}{2}CV^2 = \frac{1}{2}\frac{\varepsilon_0S}{d}E^2d^2 = \frac{\varepsilon_0 E^2}{2} V_{column} = uV_{volumn}$
* $I = neSv$
* $\tau$ average time since last collision different for different carrier
* $\sigma$ conductivity
* current density $\vec J = ne\vec v = ne \frac{eE\tau}{m} = \frac{ne^2\tau}{m}E = \sigma E$
* $I = JS = \sigma SE = \frac{\sigma S V}{L} = \frac{V}{R}$
* $R = \frac{L}{S\sigma} = \rho \frac{L}{S}$ ($\rho = \frac{1}{\sigma}$ resistivity
* Ohm's Law $V = IR$
* RC circuit
* + $-R\frac{dQ}{dt} = RI = \frac{Q}{C}$
* + $Q(t) = Q_0e^{-\frac{t}{RC}}$
* + $I(t) = -\frac{dQ}{dt} = \frac{Q_0}{RC}e^{-\frac{t}{RC}}$
* Battery
####07 Chapter End.
---
##**08**
* Emf $\epsilon = \oint \frac{\vec F_\textrm{chemical}} d\vec v$
* $\sum \Delta V = 0$
* $I$ is conserved
* RC circuit
* $Q(t)=  \epsilon C(1-e^{-\frac{t}{RC}})$
* $U_\textrm{battery} = \epsilon \int_{0}^{\infty} I(t) dt$
* $Q = I^2R = R\int_{0}^{\infty} I^2(t) dt$
###Magnetism
* Caused by moving charges
* Effect on moving charges
* Lorentz Force
* + $\vec F = q(\vec E + \vec v \times \vec B)$
* + $P = \vec F \cdot \vec v = q \vec v E +0 = q \vec v E$
* Magnetic Field <= electric current
* Cycltron
* Current loop (similar to dipole)
* + torque $\tau = BIa \cdot b\sin{theta}=\mu \times \vec B = IS \vec B$
* + $\mu$ magnetic momentum
####08 Chapter End.
---
##**09**
###Moving Charge
* $\vec F = q\,\, \vec v \times \vec B$
* For line 
* + $\vec F = \vec B IL$
* dipole(electric) - two charge
* magnetic dipole - current loop
* Electric Motor
###Current on wire
* **Biot-Savart Law**
* + The magnetic density at some point caused by current unit
* + $$dB = \frac{\mu_0}{4\pi}I\frac{dl\times \vec e_\textrm{current->point}}{|\vec R_\textrm{point} - \vec R_\textrm{current}|^2}$$
* + $\mu \approx 4\pi \times 10^{-7}$
* **Ampere Circuit Theorem**
* + $\vec B = \vec{e_{\Phi}} \frac{\mu_0 I}{2\pi R}$
* + tangent vector angle $\Phi$
* + For circle
* + $\oint_{S} \vec B d \vec r = \oint_{S} \vec B R d \Phi \vec{e_\Phi} = \mu I$
* + For any shape
* + $\oint_{S} \vec B d \vec l = \mu_0 \sum I_j$
* + right-hand law
* + $I_j$ penetrate the surface bounded by the loop
![Ampere Circuit Theorem.jpg-158.9kB][1]
####09 Chapter End.
---
##**10**
###**Ampere's Law**
* along the boundary  /  Accumulate the whole area
* $$\oint_{\partial S} \vec B \cdot d \vec \Omega = \mu_0\iint_{S} \vec J \cdot d \vec A = \mu_0 \sum I_j$$
* Symmetry
* Solenoid
* + $n$ number of turns per unit length
* + $B= \mu_0 I n$
* Doughnut
* + $N$ number of turns $\quad n = \frac{N}{2\pi R}$
* + $2\pi R B = \mu_0 I N$
* + $B =\mu_0 n I$
* Generator of electricity
* + $\epsilon = \oint \vec F_\textrm{unit charge} \cdot d \vec R = BvL$

###Faraday's Law and Lenz's Law
* motional/induced electronmotive force
* $\Phi$ loop as the boundary, the z shape unrestricted surface integral : magnetic flux
* $\epsilon = \oint_C \vec F_\textrm{em} \cdot d \vec \Omega = - \frac{d \Phi}{dt}$
* $\Phi  = \iint_{S} \vec B \cdot d  \vec A$
* $\frac{d\Phi}{dt} = -\iint \frac{\Delta \vec B}{\Delta t} \cdot d \vec A + \oint \vec v \times \vec B d \vec l$

####Faraday's Law
* $\oint \vec E \cdot d \vec l = -\iint (\frac{\partial B}{\partial t}) d \vec A$

####Lenz's Law
* Chage of magnetic flux => induce current => fight the change
####10 Chapter End.
---
##**11**
###Faraday's Law and Lenz's Law
* Betatron
* generator
* + $\Phi = A B \cos{\theta}$
* + $\epsilon =-\frac{d\Phi}{dt} = \omega AB \sin{\omega t}$
* Inductor Inductance
* $\Phi_\textrm{result} = M_{12} I_\textrm{cause}$ 
* $M$ mutual inductance $M =\mu_0 n_1 n_2 A$
* Self Inductance
* + $\Phi = LI$
* + Inductance(Henry) $L =\mu_0 n N A$
* LCR circuit
####11 Chapter End.
---
##**12**
For inductor
$V = L \frac{dI}{dt}$
For capacitor
$V = \frac{Q}{C}$
###Circuits Problem
####Recharge ULR
+ $V = \frac{Q}{C} = \frac{\int^t I dt}{C}$
+ $L\frac{d\widetilde{I}}{dt} + R \widetilde{I} + RI_\infty = V_0$
+ $I(t) = \frac{V_0}{R}(1-e^{-\frac{Rt}{L}})$
####Discharge LR
+ $L\frac{dI}{dt} + RI = 0$
+ $I  = I_0 e^{-\frac{Rt}{L}}$
+ $\int P = \int_{0}^{\infty} I^2R =  \frac{1}{2}LI^2 = U$
####Cycle LC
+ $L\frac{dI}{dt} +\frac{Q}{C} = 0$
+ $L\frac{d^2Q}{dt^2} + \frac{Q}{C} = 0$
+ $Q(t) = A \cos{\sqrt{\frac{1}{LC}}t} + B \sin{\sqrt{\frac{1}{LC}}t} = C \cos{(\omega_0t - \gamma)}$
+ $\omega_0 = \sqrt{\frac{1}{LC}}$
####~V(Alternating Voltage [AC source])LC
+ $L\frac{d^2Q}{dt^2} + \frac{Q}{C} = V_0 \cos{\omega t}$
+ $C = - \frac{\frac{V_0}{L}}{\omega^2-\omega_0^2}$
+ $Q(t) = \widetilde{C} \cos{\omega t}$
+ $I(t) = \frac{\omega \frac{V_0}{L}}{\omega^2-\omega_0^2} \sin{\omega_t}$
+ Current and Voltage not sychronized
####LCR
+ $L\frac{d^2Q}{dt^2} + R\frac{dQ}{dt} + \frac{Q}{t} = 0$
+ $Q(t) = Ae^{-\beta t}$
####~VLCR
+ $L\frac{dI}{dt} + RI + \frac{1}{C}\int^t I(t) dt = V_0 \cos{\omega t} = V(t)$
+ By conjugate and the real number property
+ $L\frac{d\overline{I}}{dt} + R\overline{I} + \frac{1}{C}\int^t \overline{I}(t) dt = \overline{V}(t)$
+ $L\frac{dRe(I)}{dt} + R\,Re({I}) + \frac{1}{C}\int^t Re({I})(t) dt = Re({V}(t))$
+ $V = V_0 e^{i\omega t}$
+ $\widetilde{I} = \widetilde{I_0} e^{i\omega t}$
+ $(R+i(\omega L - \frac{1}{\omega C}))\widetilde{I_0}e^{i\omega t} = V_0 e^{i\omega t}$
+ impedance $Z = R+i(\omega L - \frac{1}{\omega C})$
+ $\widetilde{I_0} = \frac{V_0}{Z} = \frac{V_0}{|Z|e^{i\varphi}}$
+ $\tan{\varphi} = \frac{\omega L - \frac{1}{\omega C}}{R}$
+ $\widetilde{I} = \frac{V_0}{|Z|}  e^{i(\omega t - \varphi)}$
+ $I(t) = \frac{V_0}{|Z|} \cos{(\omega t - \varphi)}$
####12 Chapter End.
---
##**13**
###~VLCR
+ When $\omega = \sqrt{\frac{1}{LC}}$ the $I$ strongest
+ complementary solution $I(t)$ is solution for LCR
+ - transient current
+ $I = \frac{V_0}{|Z|} \cos{(\omega t - \varphi)} + I_{comp}$
+ Complex ~VLCR problem
+ - Set IVP
+ - using real part
+ - See components as accumulating impendance
+ - resistor $R = R$
+ - inductor $R = i \omega L$
+ - capacitor $R = \frac{1}{i\omega C}$
+ - Then $I(t) = Re(\widetilde{I_0} e^{i \omega t})$
+ $P(t) = \frac{V_0^2}{|Z|}\cos{\omega t}\cos{(\omega t - \varphi)}$
+ draw energy and release energy
+ $\overline{P(t)} = \frac{V_0^2}{|Z|} \frac{\cos{\varphi}}{2} = \frac{1}{2} |I_0|^2R = I_\textrm{RMS}^2R$
+ $I_\textrm{RMS} = \frac{I_0}{\sqrt{2}}$
variable capacitor 
$C = \frac{\epsilon_0 A}{d}$
###Formulas
+ Gauss's Law $$\iint \vec E \cdot d \vec A =  \frac{q_\textrm{enclose}}{\varepsilon_0}$$
+ Faraday's Law $$\oint \vec E \cdot d \vec l = -\frac{d \Phi_{magnetic}}{dt}$$
+ No magnetic monopole (in always out)$$\iint \vec B \cdot d \vec A = 0$$
+ Ampere's Law(circuit theorem)$$\oint \vec B \cdot d \vec l  = \mu_0 I + \mu_0 \varepsilon_0 \iint \vec E \cdot d \vec A = \mu_0 I + \mu_0 \varepsilon_0 \frac{d \Phi_E}{dt}$$
+ - Displacement current $\varepsilon_0 \frac{d \Phi_\textrm{E(electrical flux)}}{dt}$
+ Lorentz Force$$\vec F = -q(\vec E + \vec V \times \vec B)$$
####13 Chapter End.
---
##**14**
###Wave Equation
* unit length mass $\mu$
* force $T$
* velocity of wave $v = \sqrt{\frac{T}{\mu}}$
* $y(x - vt)$
* $$\frac{\partial^2 y}{\partial x^2} - \frac{1}{v^2}\frac{\partial^2 y}{\partial t^2} = 0$$
###Maxwell Equation
[Maxwell Equation][2]
![Maxwell_1.png-20.4kB][3]
![Maxwell_2.png-19kB][4]
![Maxwell_3.png-12.5kB][5]
![Maxwell_4.png-19.7kB][6]
####14 Chapter End.
---
##**15**
###Maxwell Equation
* Wave~Light~Electric Field~Magnetic Field
* Light property
* polarization
####15 Chapter End.
---
##**16**
###Geometric Optics
* Fermat Principle
* Light travels along the shortest path of time
* + reflection: $\theta_\textrm{in} = \theta_\textrm{out}$
* + refraction: $n_1 \sin{\theta_1} = n_2 \sin{\theta_2}$
* + focusing: many shortest time path->focuses
* + - focusing mirror: parabola\ellipse\hyperbola
* + - The image position $\frac{1}{u_\textrm{object}} + \frac{1}{v_\textrm{image}} = \frac{1}{f}$
* + - ratio $M=-\frac{u}{v}$
####16 Chapter End.
---
##**17**
###Optics
* Not good parabola problem
###Lenses
* refractive index $n$
* + 1m lense = nm air
* location of object &u&
* location of image $v$
* the radius of lense $h$
* $\frac{1}{u} + \frac{1}{v} = \frac{1}{f}$
* virtual image
####17 Chapter End.
---
##**18**
###Optics
* Interference $d>>\lambda$
* Wave function (complex\differential equation) $\phi$ deviation from equilibrium
* + $L \Phi = 0$ (linear transformation)
* Then interference is addition of two wave function
* Polarization
* Principle of Huygens
####18 Chapter End.
---
##**19**
####19 Chapter End.
---
##**20**
####20 Chapter End.
---
##**21**
####21 Chapter End.
---
##**22**
####22 Chapter End.
---
##**23**
####23 Chapter End.
---
##**24**
####24 Chapter End.
---
##**25**
####25 Chapter End.
---
  [1]: http://static.zybuluo.com/Airtnp/55pmqcvavz9iizxg59nydmze/Ampere%20Circuit%20Theorem.jpg
  [2]: https://zh.wikipedia.org/wiki/%E9%A6%AC%E5%85%8B%E5%A3%AB%E5%A8%81%E6%96%B9%E7%A8%8B%E7%B5%84
  [3]: http://static.zybuluo.com/Airtnp/bgcheyrdurxx1736ischn64u/Maxwell_1.png
  [4]: http://static.zybuluo.com/Airtnp/28vi8nbzlpgrc55jou1yrtgc/Maxwell_2.png
  [5]: http://static.zybuluo.com/Airtnp/efxzux7lmbdy7kuqjb8zbsxu/Maxwell_3.png
  [6]: http://static.zybuluo.com/Airtnp/rsvw8g83eeienriytdguzebd/Maxwell_4.png