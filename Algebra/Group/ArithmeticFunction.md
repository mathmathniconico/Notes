
# 数論的函数

自然数から複素数への写像を数論的函数と呼ぶ。一見するとつまらない概念に思えるかもしれないが、自然数の整除関係を通して多くの興味深い事実を得ることができる。




## 数論的函数の為す環

__定義__ $f\colon\mathbb{N}_{1}\rightarrow\mathbb{C}$を **数論的函数** （arithmetic function）と呼び、全体を$\mathbb{A}$と表す。

- 定数函数を対応させることで$\mathbb{C}\subset\mathbb{A}$とみなせる。特に恒等的に$1$を取る数論的函数を$\mathfrak{z}$と表す。
- $\delta_{k}(k)=1$、$n\neq k$のとき$\delta_{k}(n)=0$とする。特に$k=1$のとき$\varepsilon:=\delta_{1}$と表す。

__命題__ $f, g\in\mathbb{A}$とする。これらの和$f+g$と **畳み込み** （convolution）$f\ast g$を$n\in\mathbb{N}_{1}$に対して

$$
\begin{aligned}
(f+g)(n) &:=f(n)+g(n), \\
(fg)(n) &:=\sum_{d\vert n}f(d)g\left( \frac{n}{d} \right)=\sum_{ab=n}f(a)g(b)
\end{aligned}
$$

と定める。このとき$(\mathbb{A}, +, \ast)$は$0$をゼロ、$\varepsilon$をイチとする単位的可換環である。

（証明）和に関してアーベル群となることは明らか。畳み込みは可換であり、また$\varepsilon$が乗法単位元であることも明白。

結合律を示す。$f, g, h$を数論的函数とする。$n\in\mathbb{N}_{1}$について

$$
\begin{aligned}
( (f\ast g)\ast h )(n) &=\sum_{ab=n}(f\ast g)(a)h(b)=\sum_{ab=n}\sum_{cd=a}f(c)g(d)h(b) \\
&=\sum_{cbd=n}f(c)g(d)h(b)=\sum_{ce=n}f(c)\sum_{bd=e}g(d)h(b) \\
&=\sum_{ce=n}f(c)(g\ast h)(e)=( f\ast( g\ast h) )(n)
\end{aligned}
$$

より従う。

両側分配性を示す。$f, g, h$を数論的函数とする。$n\in\mathbb{N}_{1}$について

$$
\begin{aligned}
( f\ast(g+h) )(n) &:=\sum_{d\vert n}f(d)(g+h)\left( \frac{n}{d} \right) \\
&=\sum_{d\vert n}f(d)g\left( \frac{n}{d} \right)+\sum_{d\vert n}f(d)h\left( \frac{n}{d} \right) \\
&=(f\ast g)(n)+(f\ast h)(n)
\end{aligned}
$$

より左分配性が従う。右分配性も同様である。$\square$

- $\delta_{k}\ast\delta_{l}=\delta_{kl}$が成り立つ。

__命題__ $\mathbb{A}$は整域である。

（証明）ゼロでない数論的函数$f, g$が$f\ast g=0$を満たすとする。$f, g\neq 0$より$f(a), g(b)\neq 0$となるような最小の自然数$a, b$が取れる。$d\lt a$のとき$f(d)=0$であり、$d\gt a$のとき$g(ab/d)=0$より

$$
(f\ast g)(ab)=\sum_{d\vert ab}f(d)g\left( \frac{ab}{d} \right)=f(a)g(b)\neq 0
$$

より矛盾する。$\square$

__定義__ 数論的函数$f$が畳み込みに関して可逆のとき、その逆元を$\neg f$と表す。

> 可逆な元全体$\mathbb{A}^{\times}$は乗法により群となるのであった。

__命題__ $f$を数論的函数とする。TFAE

- $f$は可逆である。
- $f(1)\neq 0$である。

（証明）$f\ast g=\varepsilon$とする。$(f\ast g)(1)=f(1)g(1)=\varepsilon(1)=1$より$f(1)\neq 0$である。

逆に$f(1)\neq 0$が成り立つとする。$g(1):=1/f(1)$として$n\gt 1$に対して

$$
g(n):=-\frac{1}{f(1)}\sum_{ab=n, b\lt n}f(a)g(b)
$$

と帰納的に定める。このとき$f\ast g=\varepsilon$が成り立つ。$\square$

> 素数を小さい順に並べて$p_{i}$とする。$n\in\mathbb{N}_{1}$に対して、$n$の$p_{i}$の指数部を$\nu_{i}(n)$で表し数列$\nu_{n}:=( \nu_{i}(n) )_{i}$を取る。このとき$f\in\mathbb{A}$に対して$\sum f(n)t^{\nu_{n}}=\sum f(n)\prod t_{i}^{\nu_{i}(n)}$を対応させる写像は形式的冪級数環$\mathbb{C}\llbracket t_{1}, t_{2}, \dotsc \rrbracket$との同型を与える。従って$\mathbb{A}$はUFDである。




## $\mathbb{A}$上の作用素

