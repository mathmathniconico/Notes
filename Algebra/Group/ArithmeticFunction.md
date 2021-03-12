
# 数論的函数

自然数から複素数への写像を数論的函数と呼ぶ。一見するとつまらない概念に思えるかもしれないが、自然数の整除関係を通して多くの興味深い事実を得ることができる。




## 数論的函数の為す環

__定義__ $f\colon\mathbb{N}_{1}\rightarrow\mathbb{C}$を **数論的函数** （arithmetic function）と呼ぶ。

- $\varepsilon(1):=1$及び$n\neq 1$について$\varepsilon(n):=0$とする。このとき$\varepsilon$は数論的函数である。

__命題__ $f, g$を数論的函数とする。これらの和$f+g$と **畳み込み積** （convolution product）$f\ast g$を$n\in\mathbb{N}_{1}$に対して

$$
\begin{aligned}
(f+g)(n) &:=f(n)+g(n), \\
(fg)(n) &:=\sum_{d\vert n}f(d)g\left( \frac{n}{d} \right)=\sum_{ab=n}f(a)g(b)
\end{aligned}
$$

と定める。このとき数論的函数全体は$\varepsilon$をイチとする単位的可換環である。

（証明）和に関してアーベル群となることは明らか。特にゼロは恒等的にゼロを取る数論的函数$0(n):=0$である。

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

より左分配性が従う。右分配性も同様である。

畳み込み積が可換なことは定義より明らか。また$\varepsilon$が乗法単位元であることも明白。$\square$

__命題__ 数論的函数全体は整域である。

（証明）数論的函数$f, g\neq 0$が$f\ast g=0$を満たすとする。$f, g\neq 0$より$f(a), g(b)\neq 0$となるような最小の自然数$a, b$が取れる。$d\lt a$のとき$f(d)=0$であり、$d\gt a$のとき$g(ab/d)=0$より

$$
(f\ast g)(ab)=\sum_{d\vert ab}f(d)g\left( \frac{ab}{d} \right)=f(a)g(b)\neq 0
$$

より矛盾する。$\square$

__定義__ 数論的函数$f$が畳み込み積に関して可逆のとき、その逆元を$f^{(-1)}$と表す。

__命題__ $f$を数論的函数とする。TFAE

- $f$は可逆である。
- $f(1)\neq 0$である。

（証明）









__例__ 以下に数論的函数の例を挙げる。

- $d(n)$は$n$の約数の個数とする。
- $\phi(n)$は$n$と互いに素な$1$以上$n$以下の整数の個数とする。（オイラーの **totient函数** と呼ぶ。）
- $L(n):=\log{n}$とする。
