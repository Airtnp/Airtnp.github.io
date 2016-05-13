---
layout:     post
title:      "Circuits Note"
subtitle:   "Too hard"
date:       2016-02-15 12:28:00
author:     "Airtnp"
header-img: "img/post-notes.jpg"
tags:
    - Notes
    - Engineering
    - Circuits
---

##01
###Circuit Abstraction

![circuit.PNG-107.9kB][1]

```flow
st=>start
op0=>condition: Lump Circuit Abstraction
op1=>condition: Amplifer Abstraction
op2=>condition: Digital Abstraction
op3=>condition: Combinational Logic Abstraction
op4=>condition: Clock-digital Abstraction
op5=>condition: Instrucation Set Abstraction
op6=>condition: Language Abstraction
op7=>condition: Software System Abstraction
sub1=>subroutine: (Analog Pad)Op-amp Abstraction
subsub1=>subroutine: Analog System Component(Oscillator/Filter/Power Supply)
sub2=>subroutine: Inverter/Combinational
Gates|invalid
sub3=>subroutine: input/output/function
sub4=>subroutine: time/clock/function
sub5=>subroutine: Computer Structure
sub6=>subroutine: Java/C/Python/PHP/Javascript(jQuery)...
sub7=>subroutine: Operating System(Linux/Windows)
e=>end

st->op0
op0(yes)->op1
op1(yes)->op2
op1(no)->sub1
sub1->subsub1
op2(no)->sub2
op2(yes)->op3
op3(no)->sub3
op3(yes)->op4
op4(no)->sub4
op4(yes)->op5
op5(yes)->op6
op5(no)->sub5
op6(yes)->op7
op6(no)->sub6
op7(no)->sub7
op7(yes)->e
```

###Maxwell Equation
![maxwell.PNG-27.7kB][2]


###Lump Abstraction Circuit
* Lump 集总（参数）电路： 满足实际电路的几何尺寸远小于工作信号波长条件的电路
* Blackbox
* + ![blackbox.PNG-10.2kB][3]
* P.S.: using $\nabla \cdot$ maxwell equation and we will get continuity electric equation
* Lumped-matter Discipline(LMD)
* + Inside Elements(wires/resistors/sources): $0 = \oint_A J\cdot dS - \oint_B J \cdot dS = \frac{\partial q}{\partial t} \Rightarrow$ $\frac{\partial q}{\partial t} = 0$
* + Outside Elements: $0 = V_{AB} = \int E_{AB} \cdot dl \Rightarrow \frac{\partial \Phi_B}{\partial t} = 0$
* Resistor
* Diode
* Photo Resistor
* Blub
* Switch
* MOSFET
* Inductors
* ($\equiv$ LMD)Kirchhoff Law
* + Kirchhoff Voltage Law (KVL)
* + - The directed sum of the electrical potential differences (voltage) around any **closed network (loop)** is zero, or:
* + - $$\sum_{k=1}^n V_k = 0$$
* + Kirchhoff Current Law (KCL)
* + - At any **node (junction)** in an electrical circuit, the sum of currents flowing into that node is equal to the sum of currents flowing out of that node
* + - $$\sum_{k=1}^n {I}_k = 0$$ (设该点电流全为流出,确定电压方向)

> 电压源可以用共集电极电路来实现，电流源可以用共基极电路来实现。例如串联型稳压电源，就是典型的电压源电路。再例如4-20毫安的电流输出单元，就是典型的电流源电路。

##02
###Basic Circuit Analysis
* Method 1: **Basic KVL, KCL**
* + Find all element v’s and i’s
* + - Associated variable discipline (set the direction)
* + write element v-irelationships(from lumped circuit abstraction)
* + - Resistor $V = IR$/Voltage Source $V=V_0$/Current Source $I=I_0$
* + write KCL for all nodes(The $i$ equations)
* + write KVL for all loops(The $v$ equations)
* + - Will have redundant equations
* Method 2: **Circuit Composition**
* + Series/Parallel Connection
* + ![circuitanalysis.PNG-13.8kB][4]
* Method 3: **Node Analysis** (Applicable on NonLinear)
* + Select reference node ($\perp$ ground)from which voltages are measured.
* + Label voltages of remaining nodes with respect to ground. These are **the primary unknowns**.
* + Write KCL for all but the groundnode, substituting device laws and KVL.
* + Solve for node voltages.
* + Back solve for branch voltages andcurrents (i.e., **the secondary unknowns**)
* + ![nodeanalysis1.PNG-19.1kB][5]
* + ![nodeanalysis2.PNG-7.4kB][6]
* + Using adjoint matrix

##03
###Circuit Analysis
* Open/Short Circuit
* Node equation: Linear, Can be written as $Ge=S$
* + $Ge=S$: Conductance Matrix|Node Voltages|Linear Sum of sources 
* Linearity $\Rightarrow$ Homogeneity Superposition
* Method 4: **Superposition Method**
* + The output of a circuit is determined by summing the responses to each source acting alone.
* Method 5: **The Thévenin Method**
* + As a blackbox
* + Replace any network with its **Thévenin Equivalence**, then solve external newwork E
* + ![thevenin1.PNG-31.5kB][7]
* + ![thevenin2.PNG-19.2kB][8]
* + Example
* + - ![eg1.jpg-36.8kB][9]
* + - ![eg2.jpg-12.9kB][10]
* + - ![eg3.jpg-13.5kB][11]
* + - ![eg4.jpg-8.1kB][12]
* + - ![eg5.jpg-7.2kB][13]
> 戴维南等效电路：
1）理想电压源可以等效为电压源与其内阻的串联形式；理想电流源可以等效为电流源与其内阻的并联形式；
2）理想电压源可以等效为电流源与其内阻并联的形式；理想电流源可以等效为电压源与其内阻的串联形式；
3）如已知电压源10V,内阻为20欧姆,则该电压源可以等效为：0.5A（10/20）电流源与其内阻20欧姆并联的形式；
4）如一只电流源1A,内阻为20欧姆,则该电流源可以等效为：20V（1*20）电压源与其内阻20欧姆串联的形式.
* Method 6: **The Norton Method**
* + ![norton.PNG-13kB][14]

##04
###Digital Abstraction
* **LCA**$\overset{Discretization}{\longrightarrow}$**DA**
* Value Discretization
* + Noise Problem (hamper the ability to distinguish between small difference in value)
* + HIGH 5V LOW   0V
* + TRUE 1  FALSE 0
* Digital System
* + ![digitalsystem.PNG-23.6kB][15]
* + IH: input high/IL: input low/OH: output high/OL: output low
* + ![sender-receiver.PNG-13.6kB][16]
* + Static Discipline
* + - Input in threshold must respond output in threshold (宁可错杀一千不可放过一个) 
* + ![sender-receiver2.PNG-24.1kB][17]
* Boolean Logic
* + Gate 
* + - AND gate 
* + - OR gate
* + - Inverter gate
* + - NAND gate
* + - ![gateand.PNG-8.7kB][18]
* + - ![gateor.PNG-10.3kB][19]
* + ![gate1.PNG-32.4kB][20]
* + ![gate2.PNG-36.8kB][21]
* + ![gate3.PNG-21.2kB][22]
* Adder Circuit
* + ![half-adder-full-adder-circuit.png-7kB][23]
> 处理模拟信号的电路称为模拟电路,处理数字信号的电路称为数字电路.模拟信号是指在时间、数值上都连续变化的信号,而数字信号则是指数值和时间两个方面都离散的信号，通常为二进制序列的信号。



##05
###Digital Gate
* Water-Faucets Analogy
* Switch Device Analogy
* + ![switch.PNG-15.1kB][24]
* + Switch Inverter Gate
* + - ![inverter.PNG-14.2kB][25]
* + Switch NAND/NOR Gate
* + - ![andor.PNG-15.6kB][26]
* + Switch AND Gate
* + - ![and2.gif-5.3kB][27]
* MOSFET Device for Switch Model
* + Metal-Oxide Semiconductor Field-Effect Transistor
* + Serve as 'Switch Model'
* + ![mosfet1.PNG-11.1kB][28]
* + ![mosfet2.PNG-16.7kB][29]
* + MOsFET Inverter Gate
* + - ![mosfetinverter.PNG-21.5kB][30]
* MOSFET Device for Switch Resistor(SR) Model
* + ![srmos.PNG-6.3kB][31]
* + ![srmosfet.PNG-16.7kB][32]
* + SR Inverter Gate
* + - ![srinverter.PNG-19.8kB][33]

##06
###NonLinear Analysis
* Linear Circuit Analysis
* + ![method.PNG-9.8kB][34]
* NonLinear Circuit Analysis
* + Eg. 
* + - ![nonlinear.PNG-14.4kB][35]
* + Analytical Method (Method 1/2/3)
* + - $$\begin{cases}  \frac{v_D-V}{R}+ & i_D & =  0 \\ & i_D & =  ae^{b_{v_D}} \end{cases}$$
* + - Node
* + Graphical Method
* + - ![nonlinear2.PNG-8.4kB][36]
* + Piecewise Linear Method
* + - Approximate curve into bunch of straight line segments
* + Incremental Method (Small Signal Method)

##07
###Incremental Analysis
* Operate at some DC offsetor bias point $V_D$, $I_D$ 
* Superimpose small signal $v_d$(music) on top of VD
* Response $i_d$ to small signal $v_d$ is approximately linear.
* ![incremental4.PNG-6.2kB][37]
* ![incremental1.PNG-28.1kB][38]
* ![incremental2.PNG-12.6kB][39]
* ![incremental3.PNG-16.4kB][40]
* ![incremental5.PNG-25.8kB][41]
* + Eg. $i_d = ae^{bV_D}\cdot b \cdot v_d = I_D \cdot b \cdot v_d$

##08
###Dependent Source
* ![dependentsource.PNG-14.4kB][42]
* 电压控制电压源（VCVS,即是英文Voltage Controlled Voltage Source的缩写，下同。）电流控制电压源（CCVS），电压控制电流源（VCCS）, 电流控制电流源（CCCS）
* + ![dependentsource3.jpg-78.4kB][43]
* + Attention: May not Linear Association
* + ![dependentsource2.PNG-13.9kB][44]
* + ![amplification.PNG-14.8kB][45]
* Realization of Dependent Source
* + ![CCVS.PNG-32.9kB][46]
* + ![CCCS.PNG-25.4kB][47]


###Amplifer
* ![amplifer.PNG-7.3kB][48]
* ![amplifer2.PNG-8.6kB][49]
* Solve Noise Tolerance
* + ![amplifernoise.PNG-10.7kB][50]
* + ![amplifernoise2.PNG-12.1kB][51]
* Solve Static Discipline
* + ![ampliferstatic.PNG-7.5kB][52]
* Amplification
* + ![amplification.PNG-14.8kB][53]
* + $\frac{\Delta v_o}{\Delta v_i} > 1$
* + Problem
* + - For $v_O>0$, VCCS consumes power: $v_O i_D$For $v_O<0$, VCCS must supply power!
* + - ![VCCS.PNG-18.4kB][54]

##09
###MOSFET Amplifer
* Switch Current Source(SCS) Model for MOSFET
* + Parasite Capacitor
* + ![mosfet.PNG-18.1kB][55]
* + DS: drain-source/GS: gate(control terminal)-source
* + The boundary of Triode and Saturation is $v_{DS} = v_{GS} - V_T$
* + More accurate than S and SR Model
* + In Saturation Region, MOSFET behaves like a current source
* + SR Model: discretization, for digital design
* + SCS Model: continuity, for analog design
* + ![scsmodel.PNG-30.4kB][56]
* MOSFET as VCCS
* + Analytic Method
* + - ![mosfetvccs.PNG-20kB][57]
* + Graphical Method
* + - ![mosfetvccs2.PNG-10.8kB][58]
* + - ![mosfetvccs3.PNG-20.7kB][59]

###Large Signal Analysis of Amplifer
* Condition: Under Saturation discipline (w/o triode/cutoff region)
* Write Transfer Function $v_{O}$ versus $v_{I}$
* Valid input operating range
* Valid output operating range
* BJT(bipolar junction transistor)


##10
###Small Signal Analysis of Amplifer
* Using Incremental Model/Linearized Model
* Graphically Method
* Mathematically Method
* + ![smallsignal.PNG-8.2kB][60]
* + $v_o = -g_mR_Lv_i$
* + $v_o = \frac{d}{dv_i} f(v_i)|_{v_i=V_i} \cdot v_i$
* + - $g_m$ is related to $V_1-V_T$, for given DC operating point voltage is constant
* Choose bias point
* Gain component $g_m \propto V_1$
* $v_i$ gets big $\rightarrow$ distortion.So bias carefully
* Input valid operating range. Bias at midpoint of input operatingrange for maximum swing

##11
###Small Signal Circuit
* Find operating point using DC bias inputs using large signal model.
* Develop small signal (linearized, perturbation) models for elements.
* Replace original elements with small signal models.
* Small Signal Components
* + ![smallsignal1.PNG-19.3kB][61]
* + ![smallsignal2.PNG-12.7kB][62]
* + ![smallsignal3.PNG-10.3kB][63]
* Amplifer Example
* + Must find operating point voltage/current (工作点)
* + ![smallsignal4.PNG-23kB][64]
* In KCL/KVL equation, seperate $V_I$ and $v_{ds}$, and get two equation


##12
###Capacitor
* MOSFET problem
* + Delay
* + Not strict discretization
* + ![mosfetproblem.PNG-22.3kB][65]
* ![capacitor.PNG-17.6kB][66]
* Ideal Linear Capacitor
* + $C = \frac{EA}{d}$
* + ![capacitor2.PNG-11.8kB][67]
* + $i = \frac{dq}{dt} = C\frac{dv}{dt}$
* RC circuit
* + By Thevenin Equivalent, every linear part of circuit can transform into $v_{TH}$ and $r_{TH}$
* + An first order (inhomogeneous) differential equation
* + ![RC.PNG-13.6kB][68]
* + $v_{hom} = Ae^{-\frac{t}{RC}}$
* + $v_{part} = c(x)v_{hom} = kRCV_1$
* + $v_C = V_1+Ae^{-\frac{t}{RC}}$

##13
###Digital Circuit Speed
* Inverter
* + Rising Delay
* + - ![risingdelay.PNG-12.9kB][69]
* + - ![risingdelay2.PNG-8.7kB][70]
* + Falling Decay
* + - ![fallingdecay.PNG-16.9kB][71]
* + - ![fallingdecay2.PNG-11.4kB][72]
* Crosstalk(串扰)
* + ![crosstalk.PNG-11.2kB][73]
* + ![crosstalk2.PNG-12.4kB][74]
* + Solved by slower transition voltage
> 串扰在电子学上是指两条信号线之间的耦合现象。这是因为空间距离近的信号线之间会出现不希望的电感性和电容性耦合从而互相干扰。电容性耦合会引发耦合电流，而电感性耦合则引发耦合电压。

##14
###State
* State: summary of past inputs relevant to predicting the future
* $v_C = f(v_C(0),v_I(t))$
* + Zero state $v_C (0) = 0$, response $V_I-V_Ie^{-t/RC}$
* + Zero input $v_I (t) = 0$, response $V_C(0)e^{-t/RC}$
* + $v_C = v_{\textrm{C,ZSR}}+V_{\textrm{C,ZIP}}$

###Memory(?)
* ![memory.PNG-22.6kB][75]
* Sampling/Storing
* First Attempt
* + add capacitor (as RC circuit)
* + ![firstatt.PNG-17.2kB][76]
* + Store pulse width: time to fill the capacitor $CR = \frac{Q}{I} (s)$
* Second Attempt
* + add buffer
* + ![secondatt.PNG-12.5kB][77]
* Third Attempt
* + add buffer + refresh
* + ![thirdatt.PNG-12.5kB][78]
* Fourth Attempt
* + add buffer + decoupled refresh
* + ![fourthattemp.PNG-9.8kB][79]
* 4-bit memory
* ![4bitmemory.PNG-21.3kB][80]

##15
###Second-Order System
* Two inverter circuit
* Parasite Inductance (act huge when little R)
* ![secondorder.PNG-20.7kB][81]
* LC circuit
* + ![LC.PNG-16.4kB][82]
* + $\omega_0 = \sqrt{\frac{1}{LC}}$
* + $j = \sqrt{-1} = i$
* + $v(t) = V_0+A_1 e^{j \omega_0 t}+A_2e^{-j \omega_0 t}$
* + $v(0)=0,\, i(0)=0$ $\Rightarrow v(t) = V_0 - \frac{V_0}{2}(e^{j\omega_0 t}+e^{-j \omega t}) = V_0(1-\cos{(omega_0 t)}$
* + $\frac{1}{2}Cv_C^2+\frac{1}{2}Li_C^2 = \frac{1}{2}CV^2$
* Method for 2nd System
* + Write DE for circuit by applying node method.
* + Find particular solution $v_P$ by guessing and trial & error.
* + Find homogeneous solution $v_H$ 
* + Total solution is $v_P+ v_H$, solve for remaining constants using initial conditions.

###Damped Second-Order System
* Using **Fourier Transform**
* RLC circuit
* + ![rlc.PNG-13.7kB][83]
* + $L\frac{dI}{dt} + RI + \frac{1}{C}\int^t I(t) dt = V_0 \cos{\omega t} = V(t)$
* + $\frac{d^2v}{dt^2}+\frac{R}{L}\frac{dv}{dt}+\frac{1}{LC}v=\frac{1}{LC}v_I$
* + ![rlc2.PNG-28kB][84]
* + $\alpha = \frac{R}{2L}$, $\omega_0 = \frac{1}{LC}$, $\omega_d = \sqrt{\omega_0^2-\alpha^2}$
* + $v(t) = V_I + A_1 e^{-\alpha t}e^{(\sqrt{\alpha^2-\omega_0^2})t}+ A_2 e^{-\alpha t}e^{(-\sqrt{\alpha^2-\omega_0^2})t}$
* + Cases
* + - $\alpha > \omega_0$ Overdamped
* + - - ![overdamped.PNG-1.6kB][85]
* + - $\alpha < \omega_0$ Underdamped
* + - - $v(t) = V_1+ A_1 e^{-\alpha t}e^{j\omega_0 t} + A_2 e^{-\alpha t}e^{-j\omega_0 t} = V_1+K_1e^{-\alpha t}\cos{(\omega_d t)}+K_2e^{-\alpha t}\sin{(\omega_d t)}$
* + - - $K_1 = -V_1$, $K_2 = -\frac{V_1 \alpha}{\omega_d}$
* + - - ![underdamped.PNG-28kB][86]
* + - $\alpha = \omega_0$ Critically-damped
* + ![damped.PNG-4kB][87]

##16
###Sinusoidal Steady State
* sinusoidal response (AC, Alternating Voltage)
* + represent the voltage by $V_I\cos{\omega t} \leftarrow V_I e^{st}$ ($s=j\omega$, $\Re e{(e^{st})} = \cos{\omega t}$)
* + ![sinusre.PNG-26kB][88]
* + $v_C = \frac{V_I}{\sqrt{1+\omega^2R^2C^2}}\cos{(\omega t+\phi)}+Ae^{-\frac{t}{RC}}$
* + - $\phi = \arctan{(-\omega RC)}$
* SSS (Sinusoidal Steady State)
* + as $t\rightarrow \infty$, transient died: $v_{hom} \rightarrow 0$
* + ![sinusre2.PNG-11.8kB][89]
* ![sinusre3.PNG-14.8kB][90]
* ![sinusre4.PNG-15.5kB][91]
* ![sinusre5.PNG-8.6kB][92]

##17
###Impedance Model
* $Z_c = \frac{1}{j\omega C}$, $V_P = V_I\frac{Z_C}{Z_C+R}$
* All As resistor, have resistance(impedance)
* ![impedance.PNG-23.7kB][93]
* ![impedance2.PNG-12.4kB][94]
* ![impedance3.PNG-20.1kB][95]
* Then KVL,KCL,superposition analysis apply
* RLC with impedance
* + ![rlc3.PNG-12.8kB][96]
* + ![RLC4.PNG-13.1kB][97]

##18
###Filter
* ![filter.PNG-4.4kB][98]
* $|H(\omega)| = \frac{|V_c|}{|V_i|}$
* ![filter2.PNG-14.7kB][99]
* ![filter3.PNG-22.3kB][100]
* BPF: band pass filter
* Selectivity
* + $1-\frac{1}{\sqrt{2}} = \frac{1}{1+j}$
* + ![selectivity.PNG-22.5kB][101]

###AM Radio
* ![amradio.PNG-13.7kB][102]
* filter out only the xHz signal

##19
###The Operational Amplifer Abstraction(?) (运算放大器)
* ![opamp.PNG-12kB][103]
* ![opamp2.PNG-11.9kB][104]
* ![opamp3.PNG-18.5kB][105]
* ![opamp4.PNG-19.6kB][106]
* Noninverting Amplifer(同相放大器)
* An VCVS, behave like ideal voltage source
* I/O depend on temperature
* Abstract differential input amplifer
* $v_o = \frac{Av_{IN}}{1+\frac{AR_2}{R_1+R_2}} \approx v_{IN} \frac{R_1+R_2}{R_2}$
* Approximation neglect the temperature cause $A$change
* Negative Feedback
* + ![opamp5.PNG-23.9kB][107]
* + Output feed back to the input
* + $\begin{cases} v^{+} \approx v^{-} \\ i^{+} \approx 0 \\ i^{-} \approx 0 \end{cases}$
* Buffer
* + ![buffer.PNG-9.5kB][108]
* + ![buffer2.PNG-10.3kB][109]

##20
###Operational Amplifer Circuit
* Method 1: Virtual Ground Method
* + $v^{+} \approx v^{-}$
* + ![opampc.PNG-20.1kB][110]
* Method 2: Superposition Method
* + ![opampc2.PNG-22.3kB][111]
* + Inverting Connection + Noninverting Connection
* Intergrator
* + ![integrator.PNG-11.1kB][112]
* + ![integrator2.PNG-24.8kB][113]
* + ![integrator3.PNG-15.6kB][114]
* Differentiator
* + ![differentiator.PNG-12.9kB][115]
* + ![differentiator2.PNG-18.6kB][116]

##21
###Op Amps Positive Feedback
* ![opampp.PNG-21.6kB][117]
* ![opampp2.PNG-23.2kB][118]
* Dynamics of op amp
* + with perturbation of op amp
* + ![dyopamp.PNG-8.7kB][119]
* + ![dyopamp2.PNG-12.2kB][120]
* + ![dyopamp3.PNG-20.2kB][121]
* + $v_o = Ke^{-\frac{t}{T}}$
* + ![dyopamp4.PNG-20.7kB][122]
* Comparator as op amp
* + ![comparator.PNG-8.2kB][123]
* + ![comparator2.PNG-16.2kB][124]
* + Hystersis
* + - ![hystersis.PNG-20.7kB][125]
* + - ![hystersis2.PNG-8.1kB][126]
* + Oscillator
* + - ![oscillater.PNG-21.3kB][127]
* + - ![oscillator2.PNG-27.3kB][128]
* + Square Wave as Clock Wave

##22
###Energy and Power
* Dissipation power
* ![energy1.PNG-10.9kB][129]
* ![energy2.PNG-7.9kB][130]
* ![energy3.PNG-8.9kB][131]
* ![energy4.PNG-11.8kB][132]
* ![energy5.PNG-10.8kB][133]
* ![energy6.PNG-19.3kB][134]
* ![energy7.PNG-19.3kB][135]
* ![energy8.PNG-19.4kB][136]
* ![energy11.PNG-9.8kB][137]
* ![energy12.PNG-5.9kB][138]
* ![energy9.PNG-22.9kB][139]
* ![energy10.PNG-15.2kB][140]

##23
###Energy and CMOS
* ![aenergy.PNG-24.7kB][141]
* ![aenergy2.PNG-12.1kB][142]
* N-Channel MOSFET(NFET)
* P-Channel MOSFET(PFET)
* + ![aenergy3.PNG-16.7kB][143]
* CMOS Inverter
* + ![aenergy4.PNG-8.1kB][144]
* + ![CMOS.PNG-19.9kB][145]
* + no path from $V_S$ to GND! no static power!
* + ![cmos2.PNG-14.4kB][146]
* CMOS NAND
* + ![cmosnand.PNG-10.1kB][147]
* ![CMOSg.PNG-24.1kB][148]

##24
###Violating the Abstraction Barrier
* Double Take
* + ![doubletake.PNG-12.3kB][149]
* + ![doubletake2.PNG-9.1kB][150]
* + ![doubletake3.PNG-15.4kB][151]
* + ![doubletake4.PNG-15.8kB][152]
* + ![doubletake5.PNG-31.4kB][153]
* Double Dip
* + ![doubledip.PNG-20.3kB][154]
* + ![doubledip2.PNG-15.6kB][155]
* + inductance on the wire caused by the current on resistor caused by square wave
* Double Team
* + ![doubleteam.PNG-21.8kB][156]
* + ![doubleteam2.PNG-16.6kB][157]
* + ![doubleteam3.PNG-18.6kB][158]
* + Waveform Engineering/Edge Smoothing
* Double Jump
* + ![doublejump.PNG-13.7kB][159]
* + ![doublejump2.PNG-15.2kB][160]

That's the END.
2016-2-15 12:28


  [1]: http://static.zybuluo.com/Airtnp/ya8lday25xyot0ixqgekiqpu/circuit.PNG
  [2]: http://static.zybuluo.com/Airtnp/bo0guw007fzrx0yfqndn95tr/maxwell.PNG
  [3]: http://static.zybuluo.com/Airtnp/5cr3v8b26fjxuqvit7r7h203/blackbox.PNG
  [4]: http://static.zybuluo.com/Airtnp/v3rp0r36jabsako62m7okwo2/circuitanalysis.PNG
  [5]: http://static.zybuluo.com/Airtnp/ityhlonu7hqyeb47pgi2opwx/nodeanalysis1.PNG
  [6]: http://static.zybuluo.com/Airtnp/3cnndn372g5skq5wpex7y6br/nodeanalysis2.PNG
  [7]: http://static.zybuluo.com/Airtnp/4rkoydxfsd9nih2b97ay67gt/thevenin1.PNG
  [8]: http://static.zybuluo.com/Airtnp/lf6tc0qyxy4w9cel0ihcmqym/thevenin2.PNG
  [9]: http://static.zybuluo.com/Airtnp/eh00jq364enbbo63e4qawcpj/eg1.jpg
  [10]: http://static.zybuluo.com/Airtnp/9pyiplc7wkfm7p7hwdkfxh2r/eg2.jpg
  [11]: http://static.zybuluo.com/Airtnp/ec58s10qtoafb4h2yw6nid7f/eg3.jpg
  [12]: http://static.zybuluo.com/Airtnp/faouxpozn3pgvc32n4pa9p9k/eg4.jpg
  [13]: http://static.zybuluo.com/Airtnp/enbcqp14j94k478yws6gvhq0/eg5.jpg
  [14]: http://static.zybuluo.com/Airtnp/uquw9zgq8ms91vla4x44p09n/norton.PNG
  [15]: http://static.zybuluo.com/Airtnp/l4vlioj311hlhyt9qc1u5i5k/digitalsystem.PNG
  [16]: http://static.zybuluo.com/Airtnp/phywuo249ssua7z0uzpybo63/sender-receiver.PNG
  [17]: http://static.zybuluo.com/Airtnp/qunqizy4gkw4x4i9rlwflo03/sender-receiver2.PNG
  [18]: http://static.zybuluo.com/Airtnp/74jgymqunklnnukkaf2jq65k/gateand.PNG
  [19]: http://static.zybuluo.com/Airtnp/zdln5elq9axcn5x5gl86zuyd/gateor.PNG
  [20]: http://static.zybuluo.com/Airtnp/v7fs6dm83t3k2exrmxxttgjp/gate1.PNG
  [21]: http://static.zybuluo.com/Airtnp/zd192fi8pw6ent5zpn9wa2g0/gate2.PNG
  [22]: http://static.zybuluo.com/Airtnp/m4f5v1cxqc53pfd24r1rs4kz/gate3.PNG
  [23]: http://static.zybuluo.com/Airtnp/5kl8s4l8i43dgz7o9sp7z50t/half-adder-full-adder-circuit.png
  [24]: http://static.zybuluo.com/Airtnp/pu62rf3iumpupd3s749mt0fy/switch.PNG
  [25]: http://static.zybuluo.com/Airtnp/vrnnkarie5gsg2hmd321idz5/inverter.PNG
  [26]: http://static.zybuluo.com/Airtnp/sccbr43bvm2isl4sbeapmxk7/andor.PNG
  [27]: http://static.zybuluo.com/Airtnp/g4kl4plme2h0948xr31i9you/and2.gif
  [28]: http://static.zybuluo.com/Airtnp/lfq2kupskt27grpy12pt228e/mosfet1.PNG
  [29]: http://static.zybuluo.com/Airtnp/rbcci8s5rl0uizue9t6qd1tx/mosfet2.PNG
  [30]: http://static.zybuluo.com/Airtnp/6x5cxzauqk51l3mwvop7duxo/mosfetinverter.PNG
  [31]: http://static.zybuluo.com/Airtnp/39dd8nmmsevn29574m7i0t05/srmos.PNG
  [32]: http://static.zybuluo.com/Airtnp/cpolsivycqdrrzu58clvvi0k/srmosfet.PNG
  [33]: http://static.zybuluo.com/Airtnp/qc6cdyxjvjjdbtrhzvnto3he/srinverter.PNG
  [34]: http://static.zybuluo.com/Airtnp/k0f6t5gqjtnfqxiwxcgx6u3h/method.PNG
  [35]: http://static.zybuluo.com/Airtnp/huqrgnr1dvbajgnehazipxdj/nonlinear.PNG
  [36]: http://static.zybuluo.com/Airtnp/i8j6mxxb6hctm83mrajwzl6m/nonlinear2.PNG
  [37]: http://static.zybuluo.com/Airtnp/lddimg16d3xd7oyhgzpvdl10/incremental4.PNG
  [38]: http://static.zybuluo.com/Airtnp/hvhthvt59xd9x3y8rplo4f02/incremental1.PNG
  [39]: http://static.zybuluo.com/Airtnp/axwne2j9tnyzxxeco1zfckob/incremental2.PNG
  [40]: http://static.zybuluo.com/Airtnp/ej9hluhonlf9ya9l6gknqgs5/incremental3.PNG
  [41]: http://static.zybuluo.com/Airtnp/katy79si7xpvmcus2eu28l2n/incremental5.PNG
  [42]: http://static.zybuluo.com/Airtnp/idajh9a331jwme25v6s0uxj7/dependentsource.PNG
  [43]: http://static.zybuluo.com/Airtnp/plrldx3d12y9jkamkcbayxut/dependentsource3.jpg
  [44]: http://static.zybuluo.com/Airtnp/0noyhot44t56vkvuay32yvln/dependentsource2.PNG
  [45]: http://static.zybuluo.com/Airtnp/nwbkpcmrv6cqsoh5t39fq7di/amplification.PNG
  [46]: http://static.zybuluo.com/Airtnp/o5kj4l61zhqbt9l9ucq2i6st/CCVS.PNG
  [47]: http://static.zybuluo.com/Airtnp/61029xkbh0z0tm1t19w5ttaz/CCCS.PNG
  [48]: http://static.zybuluo.com/Airtnp/h1fx43f0uli3t6xbct5cljfx/amplifer.PNG
  [49]: http://static.zybuluo.com/Airtnp/zkhhaqo3pwglpjt6mmubr3w7/amplifer2.PNG
  [50]: http://static.zybuluo.com/Airtnp/0psasrjzzqsjejdoe2yamqy3/amplifernoise.PNG
  [51]: http://static.zybuluo.com/Airtnp/ocofdv7ei754vadkc7ig21qw/amplifernoise2.PNG
  [52]: http://static.zybuluo.com/Airtnp/w60k24umd7j1sjlxo9sej6fn/ampliferstatic.PNG
  [53]: http://static.zybuluo.com/Airtnp/nwbkpcmrv6cqsoh5t39fq7di/amplification.PNG
  [54]: http://static.zybuluo.com/Airtnp/ewns0mggyv1r64j0l27unbvu/VCCS.PNG
  [55]: http://static.zybuluo.com/Airtnp/h3sskirza0wl0ujpjulo1nl4/mosfet.PNG
  [56]: http://static.zybuluo.com/Airtnp/gea1xqmr7meawjq6cha8hawu/scsmodel.PNG
  [57]: http://static.zybuluo.com/Airtnp/md0xfxa9d7tpzcggs5hoqs7f/mosfetvccs.PNG
  [58]: http://static.zybuluo.com/Airtnp/13gqitjus05grpowqy4b00ol/mosfetvccs2.PNG
  [59]: http://static.zybuluo.com/Airtnp/saltan6g2yyi5q19i4mt395d/mosfetvccs3.PNG
  [60]: http://static.zybuluo.com/Airtnp/j2kzog15mo5ck27txcrc6cvp/smallsignal.PNG
  [61]: http://static.zybuluo.com/Airtnp/p13bddqbwhkg0y8twupxpxu0/smallsignal1.PNG
  [62]: http://static.zybuluo.com/Airtnp/44iehr3ka3jakvk9j9g1wrgu/smallsignal2.PNG
  [63]: http://static.zybuluo.com/Airtnp/z6s35bnv2x7k4belel0vpa0t/smallsignal3.PNG
  [64]: http://static.zybuluo.com/Airtnp/h7wn7pee33yfujbcs7t2wh9r/smallsignal4.PNG
  [65]: http://static.zybuluo.com/Airtnp/t0bxqy4843wgfvsc8yedbym7/mosfetproblem.PNG
  [66]: http://static.zybuluo.com/Airtnp/xmp1ygdxw7vzbnyfs7845sin/capacitor.PNG
  [67]: http://static.zybuluo.com/Airtnp/w78tq8whztw73ygk2297f9ik/capacitor2.PNG
  [68]: http://static.zybuluo.com/Airtnp/zf31eewdwccvwipzmuijce12/RC.PNG
  [69]: http://static.zybuluo.com/Airtnp/gr6q9u4ys0vq93f5ybg1ctej/risingdelay.PNG
  [70]: http://static.zybuluo.com/Airtnp/4tut2ylxj43ntdwzkz271qsd/risingdelay2.PNG
  [71]: http://static.zybuluo.com/Airtnp/7p4fjodqnbxzs2zqnpt2rrfp/fallingdecay.PNG
  [72]: http://static.zybuluo.com/Airtnp/g248q1mmqdb3iil231sqifre/fallingdecay2.PNG
  [73]: http://static.zybuluo.com/Airtnp/2uuv1wphgmoryqyd5d4zjniu/crosstalk.PNG
  [74]: http://static.zybuluo.com/Airtnp/xabtdgz76i6wllhyl8bprodp/crosstalk2.PNG
  [75]: http://static.zybuluo.com/Airtnp/gj2tpwqf2wluy88tv9rd7xbb/memory.PNG
  [76]: http://static.zybuluo.com/Airtnp/6yiyvdn18l4no329y3j25shx/firstatt.PNG
  [77]: http://static.zybuluo.com/Airtnp/64fv9da6pfp85f57i4g7egph/secondatt.PNG
  [78]: http://static.zybuluo.com/Airtnp/502vyj0pn8xwb9k5pcrd9ixn/thirdatt.PNG
  [79]: http://static.zybuluo.com/Airtnp/t2tqv5t52fvfjtnsy1msf3d4/fourthattemp.PNG
  [80]: http://static.zybuluo.com/Airtnp/6u8c3m2ta053id94ps6h8y9w/4bitmemory.PNG
  [81]: http://static.zybuluo.com/Airtnp/f43z3kdspxu5ab6z1ae229yj/secondorder.PNG
  [82]: http://static.zybuluo.com/Airtnp/djrda6556i9ne02s6raz3r50/LC.PNG
  [83]: http://static.zybuluo.com/Airtnp/cz4jipgq7opqb2mnyrk400i2/rlc.PNG
  [84]: http://static.zybuluo.com/Airtnp/239krne6k2usaq359wxmk23s/rlc2.PNG
  [85]: http://static.zybuluo.com/Airtnp/3nueitobdh2boze34h3wap8r/overdamped.PNG
  [86]: http://static.zybuluo.com/Airtnp/r3gc6xtbjn8fngg05xdpk5df/underdamped.PNG
  [87]: http://static.zybuluo.com/Airtnp/6ve315kn1n97jo0cy1x1i602/damped.PNG
  [88]: http://static.zybuluo.com/Airtnp/k4pun29udnwflcvhpga33hm3/sinusre.PNG
  [89]: http://static.zybuluo.com/Airtnp/l6cg5dqyqo5hv3v66k05026f/sinusre2.PNG
  [90]: http://static.zybuluo.com/Airtnp/d9bnkgozh59804q0vjo0kj5j/sinusre3.PNG
  [91]: http://static.zybuluo.com/Airtnp/mni3pylfovk9ec1ot72covg0/sinusre4.PNG
  [92]: http://static.zybuluo.com/Airtnp/2plp13k38tm8d9nw8yt1i51y/sinusre5.PNG
  [93]: http://static.zybuluo.com/Airtnp/cj2eqbrhmgaro2dikc3f10eb/impedance.PNG
  [94]: http://static.zybuluo.com/Airtnp/07ipljj4ia8kshs6w992r8vp/impedance2.PNG
  [95]: http://static.zybuluo.com/Airtnp/mps5bojge9tokogkq5plwezw/impedance3.PNG
  [96]: http://static.zybuluo.com/Airtnp/1dgqdjtzaxe4klongm3ynvqb/rlc3.PNG
  [97]: http://static.zybuluo.com/Airtnp/e9z2ykih83fu2fzie9pacazi/RLC4.PNG
  [98]: http://static.zybuluo.com/Airtnp/86d0c32tnglkwwe70avh0iud/filter.PNG
  [99]: http://static.zybuluo.com/Airtnp/9xrg3cmdfzolmeifybj4vcv1/filter2.PNG
  [100]: http://static.zybuluo.com/Airtnp/oiz68takvqgkpmwj28a9t6ps/filter3.PNG
  [101]: http://static.zybuluo.com/Airtnp/w8z8xj2fq9nhkr471kxc7o0k/selectivity.PNG
  [102]: http://static.zybuluo.com/Airtnp/kymvts347z409rasqwcs6dbl/amradio.PNG
  [103]: http://static.zybuluo.com/Airtnp/gqv9u32rn1nidpdeqxncyn84/opamp.PNG
  [104]: http://static.zybuluo.com/Airtnp/8wbh057vzds93gec3d1f26x3/opamp2.PNG
  [105]: http://static.zybuluo.com/Airtnp/68tng2o1a6p8lzsog77yozuz/opamp3.PNG
  [106]: http://static.zybuluo.com/Airtnp/jwjwvgx9lo7w810zb9qrqxrd/opamp4.PNG
  [107]: http://static.zybuluo.com/Airtnp/c6p3k8sbc22llyki8kqz2ria/opamp5.PNG
  [108]: http://static.zybuluo.com/Airtnp/nqpuxmzcz7k6wc0uogv91pze/buffer.PNG
  [109]: http://static.zybuluo.com/Airtnp/eywvdae8s8oniubyrpfvj6qi/buffer2.PNG
  [110]: http://static.zybuluo.com/Airtnp/g09zfnvpbll6xqnf16dgzt26/opampc.PNG
  [111]: http://static.zybuluo.com/Airtnp/aegnqmf5rrdl2px4g4l0qdu4/opampc2.PNG
  [112]: http://static.zybuluo.com/Airtnp/b1ex9lcu8hdek3z9vjbgpui4/integrator.PNG
  [113]: http://static.zybuluo.com/Airtnp/7qfjqkc2ivr2np1718wuaey9/integrator2.PNG
  [114]: http://static.zybuluo.com/Airtnp/eyku9tbr7447mmf8u6wd1pdt/integrator3.PNG
  [115]: http://static.zybuluo.com/Airtnp/c8g5nkpved5aez80icpfsp9s/differentiator.PNG
  [116]: http://static.zybuluo.com/Airtnp/pf8co0zd0q3e76x33zrta40q/differentiator2.PNG
  [117]: http://static.zybuluo.com/Airtnp/vde5nz0tqbfk2qfyuqy0c1d1/opampp.PNG
  [118]: http://static.zybuluo.com/Airtnp/hxnwjferzt1qnubuuu9562bk/opampp2.PNG
  [119]: http://static.zybuluo.com/Airtnp/m8b18066pgdqiofpyao3jjsb/dyopamp.PNG
  [120]: http://static.zybuluo.com/Airtnp/otusleqn6rpdjq9j4vn7xai8/dyopamp2.PNG
  [121]: http://static.zybuluo.com/Airtnp/bjuik9d11u63pkegdp0yei10/dyopamp3.PNG
  [122]: http://static.zybuluo.com/Airtnp/ul38llcpr33c7npz37q26hwp/dyopamp4.PNG
  [123]: http://static.zybuluo.com/Airtnp/sdop0ohei3u5cqos1hqp08z9/comparator.PNG
  [124]: http://static.zybuluo.com/Airtnp/ce2nfff5lbn752uh1edapo3g/comparator2.PNG
  [125]: http://static.zybuluo.com/Airtnp/oph8splvp15e4bbkb2g6ec1x/hystersis.PNG
  [126]: http://static.zybuluo.com/Airtnp/k2fymvtuzjh0yqsg4kbhx4c8/hystersis2.PNG
  [127]: http://static.zybuluo.com/Airtnp/9hdgwtv36a85k36y7hosezqu/oscillater.PNG
  [128]: http://static.zybuluo.com/Airtnp/gbnnyt51o6mn7m9kvn2l9bld/oscillator2.PNG
  [129]: http://static.zybuluo.com/Airtnp/fblmhoiumr6nwfuam0g4vvz5/energy1.PNG
  [130]: http://static.zybuluo.com/Airtnp/v471vd5k1dgnqii65ykt0b7e/energy2.PNG
  [131]: http://static.zybuluo.com/Airtnp/vklp87yy05hrbk5kngpu17k8/energy3.PNG
  [132]: http://static.zybuluo.com/Airtnp/3vge6pp3n569b106rw9x7vjc/energy4.PNG
  [133]: http://static.zybuluo.com/Airtnp/0fxds799ukdysiboe67rplzd/energy5.PNG
  [134]: http://static.zybuluo.com/Airtnp/g5xoc0a6qqfvtq81xgpljmhf/energy6.PNG
  [135]: http://static.zybuluo.com/Airtnp/to6syutgmg108s4sfo5wg4qv/energy7.PNG
  [136]: http://static.zybuluo.com/Airtnp/w4kwen26y4ddbkoumkkocrx4/energy8.PNG
  [137]: http://static.zybuluo.com/Airtnp/3q334rw0d975yfj8dhlfkrgh/energy11.PNG
  [138]: http://static.zybuluo.com/Airtnp/k8frzs6e5btbfczatwabzlf6/energy12.PNG
  [139]: http://static.zybuluo.com/Airtnp/igzz1bw9a6vo80ubj6j8hgvo/energy9.PNG
  [140]: http://static.zybuluo.com/Airtnp/rui74rf2dhcvzofztbu6zosc/energy10.PNG
  [141]: http://static.zybuluo.com/Airtnp/j7vxm2hcubopfjofgwvn7i4p/aenergy.PNG
  [142]: http://static.zybuluo.com/Airtnp/4v992aou0attsvddn3ddoxih/aenergy2.PNG
  [143]: http://static.zybuluo.com/Airtnp/djmouztykg6groqpfbudejh8/aenergy3.PNG
  [144]: http://static.zybuluo.com/Airtnp/nzyeypbpgf17nxrgpfn9v15u/aenergy4.PNG
  [145]: http://static.zybuluo.com/Airtnp/06zwy2cc7oqtq9c8m4j277uj/CMOS.PNG
  [146]: http://static.zybuluo.com/Airtnp/q7vx8av6y3gt4r75kma55n1q/cmos2.PNG
  [147]: http://static.zybuluo.com/Airtnp/6bhgyu5yrfwaux87q4nqhvlr/cmosnand.PNG
  [148]: http://static.zybuluo.com/Airtnp/y8a251kah6fy4lnahz2l761x/CMOSg.PNG
  [149]: http://static.zybuluo.com/Airtnp/uzbiv8iao8u0g5f5msjzznit/doubletake.PNG
  [150]: http://static.zybuluo.com/Airtnp/c1iow2i1c5n59myma5mgh5lr/doubletake2.PNG
  [151]: http://static.zybuluo.com/Airtnp/xmnhlvtpyr1otk8xfg3hi7ap/doubletake3.PNG
  [152]: http://static.zybuluo.com/Airtnp/wo10kz33hpru7ltioldrxgis/doubletake4.PNG
  [153]: http://static.zybuluo.com/Airtnp/hbf2gk52fnr0uiw3dl0n7gn4/doubletake5.PNG
  [154]: http://static.zybuluo.com/Airtnp/34es0go9gt63xafimtv3pjbo/doubledip.PNG
  [155]: http://static.zybuluo.com/Airtnp/84tlo1yauonn3gfvurb6qr07/doubledip2.PNG
  [156]: http://static.zybuluo.com/Airtnp/1m6gm58hs4lfo0z699abspys/doubleteam.PNG
  [157]: http://static.zybuluo.com/Airtnp/kdklyjdtsbymzmp7vwar83mw/doubleteam2.PNG
  [158]: http://static.zybuluo.com/Airtnp/znhhh5itpuvc4lyrqbbtn6pt/doubleteam3.PNG
  [159]: http://static.zybuluo.com/Airtnp/0npympg117lsfbmgu5cz3pt0/doublejump.PNG
  [160]: http://static.zybuluo.com/Airtnp/0p4zko6cxoq2qzik3n4966o6/doublejump2.PNG