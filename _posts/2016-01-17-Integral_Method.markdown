---
layout:     post
title:      "积分方法"
subtitle:   "自娱自乐"
date:       2016-01-07 11:38:00
author:     "Airtnp"
header-img: "img/post-notes.jpg"
tags:
    - Notes
    - Math
    - Integral
---


##不定积分
###特殊形式积分
* $\int P(x)Q(x) dx \Leftrightarrow \int uv^{n-1} dx$ 形式， 其中 $ P(x)=\left\{
\begin{aligned}
x & =  e^{kx} & （微分不变，可回头） \\
y & =  \sin(\omega t + \varphi) & （微分两次不变，可回头递推） \\
z & = \sum a_nx^n & （多项式微分消次数）
\end{aligned}
\right.
$ $$\int uv^{(n+1)} = \sum_{i = 1}^{n} (-1)^{(i)}u^{(i)}v^{(n+1-i)} + (-1)^{n+1}\int u^{(n+1)}v$$
###分部积分
* 反对幂三指
* $$\arcsin{(x)},\,\ln{(x)},\,x^n,\, \sin{(\omega t +\varphi)},\,e^{kx} $$
 $$\int \arctan{(x)}e^{kx} = \frac{1}{k}\int \arctan{(x)}de^{kx} = \frac{1}{k}e^{kx}\arctan{(x)} - \frac{1}{k}\int \frac{e^{kx}}{1+x^2} dx$$
（这个例子玩脱了...这个应该是不可积函数..反正就是顺序问题）
（经验规律-由初等函数复杂性总结）

###有理因式分解
 $$\frac{1}{x^3+1} = \frac{A}{x+1} + \frac{B}{x^2-x+1}$$
(此时由系数关系， [$deg(A)$ :A的次数] $\deg{A} = 1 \,\, \deg{B} = 0 \Rightarrow $分子零次）
###代换
 * **凑微分** $$\int f(x) dx = k\int g'(x)g(x)dx$$
 * + 题目凑好的...
 * **三角代换** 
 * + $$f(a^2-x^2) \Rightarrow x=a\sin{\theta} ,\, x = a\cos{\theta}$$
 * + $$f(a^2+x^2) \Rightarrow x=a\tan{\theta}$$
 * + $$f(x^2-a^2) \Rightarrow x=a\sec{\theta} ,\, x = a\csc{\theta}$$
 * + $\sin^{2k}{\theta}$ 倍角公式
 * + 同理有双曲代换 由$1+\sinh^2{x} = \cosh^2{x}$ 和 $\tanh^2{x} = sech^2{x}-1$
 * + **万能代换**
$$t = \tan{\frac{\theta}{2}}$$
$$\sin{x} = \frac{2\sin{\frac{x}{2}}\cos{\frac{x}{2}}}{\sin^2{\frac{x}{2}}+\cos^2{\frac{x}{2}}} = \frac{2t}{1+t^2}$$
        $$\cos{x} = \frac{\cos^2{\frac{x}{2}}-\sin^2{\frac{x}{2}}}{\sin^2{\frac{x}{2}}+\cos^2{\frac{x}{2}}} = \frac{1-t^2}{1+t^2}$$
$$x = 2\arcsin{t} \Rightarrow d{x} = \frac{2}{1+t^2} d{t}$$
* + - 万能代换改变了次数$\Rightarrow$用于$a+b\sin{\theta}$
* **指数代换** $$x = t^{\alpha}$$
* + 指数代换调节次数$\Rightarrow$齐次
* + **倒代换** $$\alpha = -1 \Rightarrow x = \frac{1}{t}$$
* + - 倒代换改变了次数$\Rightarrow$用于$a+bx^k$
* **无理代换**
$$t = \sqrt{f(x)} \Rightarrow x = f^{-1}(t^2)$$
* + 无理代换可以直接提出$\frac{f(x)}{\sqrt{g(x)}}$中的有理分式
* + 无理代换可能将无理式变为有理式
* + $\frac{x^2}{\sqrt{1-x^2}} = \frac{1}{t} - t\,\,\,(t = \sqrt{1-x^2})$
* **Euler代换** $$\deg{f(x)}=2 \Rightarrow \sqrt{f(x)} = ax-t$$
$$a>0 \Rightarrow \sqrt{a^2+bx+c} = \pm \sqrt{a}x + t \Rightarrow x = \frac{t^2-c}{b\pm2\sqrt{a}t}$$
$$c>0 \Rightarrow \sqrt{a^2+bx+c} = tx \pm \sqrt{c} \Rightarrow x = \frac{b\pm2\sqrt{c}t}{t^2-a}$$
$$ax^2+bx+c=a(x-\alpha)(x-\beta) \Rightarrow \sqrt{a^2+bx+c} = t(x-\alpha) \Rightarrow x = \frac{\alpha\beta - \alpha t^2}{a-t^2}$$
* + Euler代换将二次无理式变为有理式
* **代换总结**
* + 无理$\Rightarrow$有理
* + 非齐次$\Rightarrow$齐次
###升维
>$$A=\int_{-\infty}^{\infty}e^{-x^2}\mathrm{d}x$$
似乎并不会积，但我们增加一个维度y，变为
$$A^2=\iint_{-\infty}^{\infty}e^{-x^2-y^2}\mathrm{d}x\mathrm{d}y=\int_{0}^{2\pi}\mathrm{d}\theta\int_{0}^{\infty}r\mathrm{d}re^{-r^2}$$
就很容易了，解得$A^2=2\pi\frac{-e^{-r^2}}{2}\bigg|_0^{\infty}=\pi$，即$A=\int_{-\infty}^{\infty}e^{-x^2}\mathrm{d}x=\sqrt{\pi}$
（当然出于严格性的要求其实还要用极限逼近一下）
稍复杂一点的实数积分或求和，很多都可以延拓到复平面上用复变函数的方法做。

 

##定积分
###对称性
* 奇函数/周期性
$\int_{0}^{\pi/2} f(\sin{x})dx = \int_{0}^{\pi/2} f(\cos{x}) \,\mathbb{dx}$
$\int_{0}^{\pi} f(\sin{x})dx = 2\int_{0}^{\pi/2} f(\sin{x}) \,\mathrm{dx}$
$\int_{0}^{\pi} xf(\sin{x})dx =  \frac{\pi}{2}\int_{0}^{\pi} f(\sin{x}) \,\mathrm{dx}$

###由级数导出
* 在收敛域中 $\int_{a}^{b} \sum_{n = 0}^{\infty}  f_n(x) dx = \sum_{n = 0}^{\infty} \int_{a}^{b} f_n(x) dx$
* $$\int_{a}^{b} f(x) dx = \sum_{n = 0}^{\infty} \int_{a}^{b} f_n(x) dx = \sum_{n = 0}^{\infty} k_n(x)(b^n-a^n)$$
* 例:
$\int_{0}^{1} x^x d{x} = \sum_{n = 0}^{\infty}\frac{(-x)^n}{(n+1)^n}$
$x^x = e^{x\ln{x}} = \sum_{n = 0}^{\infty} \frac{(x\ln{x})^n}{n!}$
$\int_{0}^{1} x^x d{x} = \sum_{n = 0}^{\infty} \int \frac{(x\ln{x})^n}{n!} d{x}$
$\int_{0}^{1} x^n \ln^n{x} d{x} = \frac{1}{n+1}\int_{0}^{1} \ln^n{x} d{x^{n+1}} = x^{n+1}\ln^n{x}|_{0}^{1} - \frac{1}{n+1}\int_{0}^{1} x^{n+1}\ln^{n-1}{x} d{x}$
$=(-1)^n\frac{n!}{(n+1)^{n}}\int_{0}^{1} x^{n+1} d{x} = (-1)^n\frac{n!}{(n+1)^n}$
$\int_{0}^{1} x^x d{x} = \sum_{n = 0}^{\infty} \int \frac{(x\ln{x})^n}{n!} d{x} = (-1)^n \frac{x^n}{(n+1)^n}$


